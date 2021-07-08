<template>
    <div>
        <div class="normal">
            <span>帅哥</span>
        </div>
        <button @click="send">sendEmit</button>
    </div>

</template>

<script>
export default {
    name: "Son",
    methods:{
        send(){
            this.$emit("sendEmit",100);
        }
    }
}
</script>

<style scoped lang="stylus">
    .normal
        span:before
            content:"<<"
            color:red
        span:after
            content ">>"
            color:red
        &:hover
            filter brightness(1.3)

</style>
