<template>
  <div class="about">
        {{arr1}}
      {{arr2}}
      <button @click="concatArray">拼接数组</button>
      <button @click="reverseArray">反转数组</button>
      <button @click="maxBy">取数组中最大值</button>
      <button @click="cloneDeep">深拷贝数组</button>
  </div>
</template>

<script>

    export default {
        name: 'About',
        data(){
            return{
                arr1:[1,2,3,4,5,6,7],
                arr2:[110,120,130],
                arr3:[{'a':1},{'a':2},{'a':3}],
                arr4:[{name:'a',value:100},{name:'b',value:200}]
            }
        },
        methods:{
            concatArray(){
                this.arr1 = _.concat(this.arr1,6,5,4,3,2,1)
            },
            reverseArray(){
                let resultArray = _.reverse(this.arr2);
                console.log(resultArray)
            },
            maxBy(){
                let resultArray = _.maxBy(this.arr3,(item)=>{
                    return item.a
                })
                console.log(resultArray)
            },
            cloneDeep(){
                let resultArray = _.cloneDeep(this.arr4)
                console.log(resultArray)
                console.log(this.arr4 === resultArray)
            },
            forOwnTest(){
              //lodash用于遍历对象属性的方法
                let FOO = {
                  a:1,
                  b:2
                }
                _.forOwn(FOO,(value,key)=>{
                  console.log(key,value)
                })
            },
            assignTest(){
              //lodash中的指派方法，将源对象的属性融合进目标对象，若有相同的属性key，则用源对象的替换掉目标对象的
              let FOO = {
                a:1
              }
              let test1 = {
                a:'niubi'
              }
              let test2 = {
                b:'shuai'
              }
              let test3 = {
                c:'test3'
              }
              let result = _.assign(FOO,test1,test2,test3)
              console.log(result)
            }
        },
        mounted() {
            // this.concatArray();
            // this.forOwnTest();
          this.assignTest();
        }
    }
</script>


<style lang="stylus">
.about
    font-family Avenir, Helvetica, Arial, sans-serif
    -webkit-font-smoothing antialiased
    -moz-osx-font-smoothing grayscale
    text-align center
    color #2c3e50
    margin-top 60px
</style>
