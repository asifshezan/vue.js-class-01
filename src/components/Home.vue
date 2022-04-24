<template>
    <div>
        <!-- <h1>{{ data }}</h1>-->
        <h2 v-if="show">Condition in Vue.Js</h2>
        <h2 v-else>Condition in Else block</h2>
        <button v-on:click="hi">Show Hi Function</button>
        <button v-on:mouseover="hi">Show Hi Function</button>
        <button v-on:click="display">Toggle Element</button>
    </div>
</template>
<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name:'Home',
    props:{
        data:String,
        // msg:String,
    },methods: {
        hi(){
            console.log("Everything is alright.")
            alert("I want to get up in this world.")
        },display(){
            this.show=!this.show
        }
    },data(){
        return {show:true}
    }
};
</script>