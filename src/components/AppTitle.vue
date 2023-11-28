<script >
import axios from "axios"
export default{
    created(){
    
},
created(){
    
    this.getCharacters()
},
methods: {
    getCharacters(){ 
        axios
        .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
        .then(resp =>{
            console.log(resp);
        })
    }
},
}

</script>

<template>
<section>
    <h2 class="mx-5">Yu-Gi- Oh Api</h2>
</section>   

</template>

<style lang="scss" scoped>
section{
   display: flex;
   align-items: center;
   background-color: white;

}
</style>