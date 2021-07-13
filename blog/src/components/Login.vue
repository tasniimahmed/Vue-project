<template>
    <div class="child">
    <h1>Login Form</h1>
    <input type="text" v-model= "loginForm.username" placeholder="Enter user name"/><br><br>
    <input type="password" v-model= "loginForm.password" placeholder="Enter user password"/><br><br>
    <button v-on:click = "getlogin() ">Login</button>
    </div>
</template>

<script>

export default {
   name: 'Login',
   data(){
       return{
           loginForm:{
               username:null,
               password:null
           }
       }
   },
   methods:{
       getlogin(){
           console.log("getlogin is called", this.loginForm.username)
       }
   }
}
</script>

<style scoped>
    .child{
        background-color: rgb(163, 189, 206);
        height: 500px;
    }
</style>