<template>
    <button @click="send">sendEmit</button>
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

<style scoped>

</style>
