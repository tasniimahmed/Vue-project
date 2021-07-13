<template>
    <div>
    <h1>Hello from Home Component</h1>
    <h1>{{data}}</h1>
    <h1>{{msg}}</h1>
    <button v-on:mouseover="hello('dataa')">call hello</button>
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
        hello(item){
            //note: events as: click, mouseover
            alert(item)
        }
    }
}
</script>
