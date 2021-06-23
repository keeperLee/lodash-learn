<template>
  <div class="about">
        {{arr1}}
      <button @click="concatArray">拼接数组</button>
  </div>
</template>

<script>

    export default {
        name: 'About',
        data(){
            return{
                arr1:[1,2,3,4,5,6,7]
            }
        },
        methods:{
            concatArray(){
                this.arr1 = _.concat(this.arr1,6,5,4,3,2,1)
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
