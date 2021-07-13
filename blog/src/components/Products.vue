<template>
    <div class="child">
    <h1>Products Component</h1>
    <h2>{{name}}</h2>
    </div>
</template>

<script>

export default {
   name: 'Products',
   //el var el parent hyb3tholi
   props: ['name']
}
</script>

<style scoped>
    .child{
        background-color: rgb(119, 119, 119);
        height: 100px;
        width: 200px;
        padding: 30px;
        margin: 20px;
    }
</style>