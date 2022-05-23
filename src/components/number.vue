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
    components:{
        imge,
    },
    data(){
        return{
            count: 0,
            color: "colorchange_red",            
        }
    },
    methods:{
        colorChange(){
            if(this.color=="colorchange_red"){
                this.color = "colorchange_blue";
            }
            if(this.color=="colorchange_blue"){
                this.color="colorchange_red";
            }
            this.count++
        }
    }


}
</script> 

<template>
  <h1 style="text-align: center; font-size:80px;">{{ msg }}</h1>
  <div :id="color" v-on:wholeclick="colorChange">{{ count }}</div>
  <imge @wholeclick="colorChange"></imge>
</template>

<style>

#colorchange_red{
    color: red;
    text-align: center;
    font-size: 50px;
    font-family: Arial, Helvetica, sans-serif;
}
#colorchange_blue{
    color: blue;
    text-align: center;
    font-size: 50px;
    font-family: Arial, Helvetica, sans-serif;
}

</style>