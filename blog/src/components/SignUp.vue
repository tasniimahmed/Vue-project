<template>
    <div class="child">
    <h1>Sign up Form</h1>
    <input type="text" v-model= "signupForm.username" placeholder="Enter user name"/><br><br>
    <input type="password" v-model= "signupForm.password" placeholder="Enter user password"/><br><br>
    <p>Hobbies</p>
    <input type="checkbox" v-model= "signupForm.hobbies" value="travel" id="travel" />
    <label for="travel">Travel</label><br>
    <input type="checkbox" v-model= "signupForm.hobbies" value="sports" id="sports" />
    <label for="sports">Sports</label><br>
    <button v-on:click = "signupuser() ">Sign Up</button>
    </div>
</template>

<script>

export default {
   name: 'SignUp',
   data(){
       return{
           signupForm:{
               username:null,
               password:null,
               hobbies:[]
           }
       }
   },
   methods:{
       signupuser(){
           console.log("signup is called", this.signupForm.hobbies)
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