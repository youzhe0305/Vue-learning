
<script>
export default {
    name:"imge",
    data(){
        return{
            ifpop:0,    
            imgsrc:"../assets/No.jpg",    
        }
    },
    methods:{
        imgclick(){
            if(ifpop==0){
                this.imgsrc = "../assets/Yeah.jpg";
                this.ifpop=  1;
            }
            else if(ifpop==1){
                this.imgsrc = "../assets/No.jpg";
                this.ifpop = 0;
            }
            this.$emit("wholeclick")
        }
    }
}
</script>
<template>
    <img src="imgsrc" id="backimg" @click="imgclick()">
</template>
<style>
    #backimg{
        width:100% ;
        height:100%;
        z-index: -1;
    }
</style>


