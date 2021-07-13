<template>
    <div>
    <h1>Hello from Home Component</h1>
    <h1>{{data}}</h1>
    <h1 v-if="show">{{msg}}</h1>
    <h1 v-else> Else part</h1>
    <button v-on:click="display()">Display</button>
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
            show:false
        }
    }
}
</script>
