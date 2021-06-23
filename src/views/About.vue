<template>
  <div class="about">
        {{arr1}}
      {{arr2}}
      <button @click="concatArray">拼接数组</button>
      <button @click="reverseArray">反转数组</button>
  </div>
</template>

<script>

    export default {
        name: 'About',
        data(){
            return{
                arr1:[1,2,3,4,5,6,7],
                arr2:[110,120,130]
            }
        },
        methods:{
            concatArray(){
                this.arr1 = _.concat(this.arr1,6,5,4,3,2,1)
            },
            reverseArray(){
                let resultArray = _.reverse(this.arr2);
                console.log(resultArray)

            }
        },
        mounted() {
            // this.concatArray();
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
