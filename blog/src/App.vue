<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
   <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
   <!-- <home data= "Tasnim is here" msg= "good"/> -->
   <!--<Login />--> 
   <SignUp/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import Home from './components/Home.vue'
//import Login from './components/Login.vue'
import SignUp from './components/SignUp.vue'

export default {
  name: 'App',
  components: {
   // Login,
    SignUp
    //HelloWorld,
    //Home
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
