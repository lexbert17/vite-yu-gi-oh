<script >
import AppTitle from './components/AppTitle.vue';
import AppCharactersList from './components/AppCharactersList.vue';
import { store } from "./store";
import axios from 'axios';
import AppSelect from './components/AppSelect.vue';
export default{
components:{ AppTitle, AppCharactersList, AppSelect },
data() {
  return{
    store:store,

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
    },
  
    handleSelect(){
      console.log("ciao");
      axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?", {
        params: {
          archetype: this.store.selectOption,
        }
      })
      .then((resp) => {
        this.store.cardList = resp.data.data;
      })
    }
},

}

</script>

<template>
<AppTitle/>
<AppSelect @performSelect="handleSelect"/>
<AppCharactersList/>


</template>

<style  lang="scss">
@use"./style/general.scss";

body{
  background-color: orange;
}
</style>
