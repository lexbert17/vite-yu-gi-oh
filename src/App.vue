<script >
import AppTitle from './components/AppTitle.vue';
import AppMain from './components/AppMain.vue';

export default{
components:{AppTitle, AppMain}
}
</script>

<template>
  <AppTitle/>
<AppMain/>


</template>

<style  lang="scss">
@use"./style/general.scss";

body{
  background-color: orange;
}
</style>
