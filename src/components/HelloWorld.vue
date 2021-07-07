<template>
    <div class="iCountUp">
<!--        <ICountUp-->
<!--                :startVal="startVal"-->
<!--                :endVal="endVal"-->
<!--                :options="options"-->
<!--                @ended="changeValue"-->
<!--        />-->
        <Son @sendEmit="receiveValue"></Son>
    </div>
</template>

<script type="text/babel">
// import ICountUp from 'vue-countup-v2';
import Son from './Son.vue'
export default {
    name: 'demo',
    components: {
        // ICountUp
        Son
    },
    data() {
        return {
            startVal: 300,
            endVal: 500,
            options: {
                useEasing: false,
                useGrouping: true,
                separator: ',',
                decimal: '.',
                prefix: '',
                suffix: '',
                duration:10
            }
        };
    },
    methods: {
        changeValue: function(instance, CountUp) {
            alert(1110)
        },
        receiveValue(value){
            alert(value)
        }
    }
};
</script>

<style scoped>
.iCountUp {
    font-size: 12em;
    margin: 0;
    color: #4d63bc;
}
</style>
