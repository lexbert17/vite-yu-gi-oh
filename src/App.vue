<script >
import AppTitle from './components/AppTitle.vue';
import AppCharactersList from './components/AppCharactersList.vue';
import { store } from "./store";
import axios from 'axios';
export default{
components:{ AppTitle, AppCharactersList },
data() {
  return{
    store:store
  }
},
created(){
this.getCharacters();
},
methods: {
    getCharacters(){ 
        axios
        .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
        .then(resp =>{
            this.store.cardList = resp.data.data
            
        });
    }
},

}

</script>

<template>
<AppTitle/>
<AppCharactersList/>


</template>

<style  lang="scss">
@use"./style/general.scss";

body{
  background-color: orange;
}
</style>
