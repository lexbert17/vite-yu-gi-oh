<script>
export default{
      props:{
        character: Object
      }  
}
</script>

<template>
<div class="card mb-2 h-100" style="width: 18rem;">
  <img :src="character.card_images[0].image_url_small" class="card-img-top" alt="character.name">
  <div class="card-body">
    <h5 class="card-title">{{character.name}}</h5>
    <p class="card-text">{{ character.archetype ? character.archetype : "--"}}</p>
  </div>
</div>
</template>

<style lang="scss" scoped>

</style>