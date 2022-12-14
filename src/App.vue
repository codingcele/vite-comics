<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppMerchandise from './components/AppMerchandise.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppContent,
    AppMerchandise,
  }
}

</script>

<template>
  <AppHeader />
  <AppContent />
  <AppMerchandise />
</template>

<style lang="scss">
/* @use "./styles/partials/variables" as *;
@use "./styles/general.scss" as *; */
* {
  box-sizing: border-box;
  margin: 0px;
  font-family: Verdana;
}
</style>
