<script>
import { store } from "../store";
export default{
       data(){
        return{
            store,
        };
       } 
}
</script>

<template>
<section class="flex ">
    <select name="archetipo" id="archetype" @change="$emit( 'performSelect' )" v-model="store.selectOption" >
  <option value="alien">Alien</option>
  <option value="Ally of Justice">Ally of Justice</option>
  <option value="Ancient Gear">Ancient Gear</option>
</select>
</section>
</template>

<style lang="scss" scoped>
select{
    margin: 2rem 5rem;
    width: 150px;
    height: 40px;
    border-radius: 10px;

}
</style>