<script>

import imge from "./image.vue"
export default {
    name:"num",
    props:{
        msg: {
            type:String,
            default:"defult word",
        }

    },
    data(){
        return{
            count: 0,
            color: "red",            
        }
    },
    methods:{
        colorChange(){
            if(this.color=="red"){
                color = "blue"
            }
            if(this.color=="blue"){
                color="red";
            }
            count++
        }
    }


}
</script> 

<template>
  <h1>{{ msg }}</h1>
  <div :color="color" v-on:wholeclick="colorChange">{{ count }}</div>
  <imge></imge>
</template>

<style>

</style>