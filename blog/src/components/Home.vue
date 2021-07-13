<template>
    <div>
    <h1>Hello from Home Component</h1>
    <h1>{{data}}</h1>
    <h1 v-if="show">{{msg}}</h1>
    <h1 v-else> Else part</h1>
    <button v-on:click="display()">Display</button>

    <h1>looping</h1>
    <table border="2px;">
    <tr>
        <td>ID</td><td>Name</td><td>Email</td>
    </tr>
    <tr v-for= "user in users" :key="user.id">
        <td>{{user.id}}</td><td>{{user.name}}</td><td>{{user.email}}</td>
    </tr>
    </table>
    </div>
</template>

<script>

export default {
   name: 'Home',
   props: { 
       data: String,
       msg: String
    },
    methods:{
        display(){
            //note: events as: click, mouseover
            //alert(item)
            
            //this.show= true

            //toogling
            this.show= !this.show
        }
    },
    data(){
        return{
            show:false,
            users:[
                { id:1, name:'peter', email: 'peter@gmail.com'},
                { id:2, name:'thomas', email: 'thomas@gmail.com'},
                { id:3, name:'tasnim', email: 'tasnim@gmail.com'}
            ]
        }
    }
}
</script>
