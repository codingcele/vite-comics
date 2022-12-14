<script>
import AppHeader from './components/AppHeader.vue';

export default {
  name: "App",
  components: {
    AppHeader,
  }
}
</script>

<template>
  <AppHeader />
</template>

<style lang="scss">
/* @use "./styles/partials/variables" as *;
@use "./styles/general.scss" as *; */
* {
  box-sizing: border-box;
  margin: 0px;
}
</style>
