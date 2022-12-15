<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppMerchandise from './components/AppMerchandise.vue';
import AppLists from './components/AppLists.vue';
import AppLine from './components/AppLine.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppContent,
    AppMerchandise,
    AppLists,
    AppFooter,
    AppLine,

  }
}

</script>

<template>
  <AppHeader />
  <AppContent />
  <AppMerchandise />
  <AppLists />
  <AppFooter />
  <AppLine />
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
