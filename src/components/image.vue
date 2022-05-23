
<script>
export default {
    name:"imge",
    data(){
        return{
            ifpop:0,    
            imgsrc: "/src/assets/No.jpg",    
        }
    },
    methods:{
        imgclick(){
            if(this.ifpop==0){
                this.imgsrc = "/src/assets/Yeah.jpg";
                this.ifpop=  1;
            }
            else if(this.ifpop==1){
                this.imgsrc = '/src/assets/No.jpg';
                this.ifpop = 0;
            }
            this.$emit("wholeclick")
            console.log(this.$emit)
        }
    }
}
</script>
<template>
    <img :src="imgsrc" id="backimg" @click="imgclick()">
</template>
<style>
    #backimg{
        width:100% ;
        height:100%;
        z-index: -1;
    }
</style>


