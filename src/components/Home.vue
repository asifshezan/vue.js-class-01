<template>
    <div>
        <!-- <h1>{{ data }}</h1>-->
        <h2 v-if="show">Condition in Vue.Js</h2>
        <h2 v-else>Condition in Else block</h2>
        <button v-on:click="hi">Show Hi Function</button>
        <button v-on:mouseover="hi">Show Hi Function</button>
        <button v-on:click="display">Toggle Element</button><br>
        <table cellpadding="0" sellspacing="0" border="1">
            <tr>
                <th>Id</th>
                <th>Name</th>
                <th>Email</th>
            </tr>
            <tr v-for="user in users" :key="user.id">
                <td>{{ user.id }}</td>
                <td>{{ user.name }}</td>
                <td>{{ user.email }}</td>
            </tr>
        </table>
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
    },data() {
        return {
            users:[
                {id:1, name:'Asif', email:'asif@gmail.com'},
                {id:2, name:'Tur', email:'tur@gmail.com'},
                {id:3, name:'Toki', email:'toki@gmail.com'},
                {id:4, name:'Nuha', email:'nuha@gmail.com'}
            ]
        }
    },
};
</script>