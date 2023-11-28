<script>
import {store} from "../store"
import AppCharacterCard from "./AppCharacterCard.vue";
export default{
    data() {
        return {
            store: store
        };
    },
    components: { AppCharacterCard }
}
</script>

<template>
    <section class="container mt-5">
        <h2>lista personaggi</h2>
        <div class="row row-cols-4 g-3">
            <div class="col" v-for="character in store.cardList">
            <AppCharacterCard :character="character" />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
section {
color: green;
background-color: white;
}

</style>