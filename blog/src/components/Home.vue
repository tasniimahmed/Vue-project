<template>
    <div class="home">
    <h1>Home Component</h1>
    <h1>{{name}}</h1>
    <p v-html="header"></p>
    <h3>{{ok?"yes":"no"}}</h3>
   <!-- <h1>{{data}}</h1>
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
    </table> -->
    <Users/>
    <Products/>
    </div>
</template>

<script>
import Users from './User.vue'
import Products from './Products.vue'

export default {
   name: 'Home',
    components: {
    Users,
    Products
  },
   props: { 
       data: String,
       msg: String
    },
    methods:{
        display(){
            //note: events as: click, mouseover
            //alert(item)
            
            //this.show= true
            //this.name="Mona"
            //toogling
            this.show= !this.show
        }
    },
    data(){
        return{
            header: "<h2>Added by js</h2>",
            ok:true,
            name: 'Tasnim',
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

<style scoped>
    .home{
        background-color: rgb(163, 189, 206);
        height: 500px;
    }
</style>