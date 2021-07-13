<template>
    <div class="child">
    <h1>Users Component</h1>
    <button v-on:click="updateTitle">change title</button>
    </div>
</template>

<script>

export default {
   name: 'Users',
   methods:{
       updateTitle(){
           //change title is the name of the event
           this.$emit('changeTitle', 'props changd')
       }
   }
}
</script>

<style scoped>
    .child{
        background-color: rgb(192, 192, 192);
        height: 100px;
        width: 200px;
        padding: 30px;
        margin: 20px;
    }
</style>