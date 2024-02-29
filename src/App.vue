<script>
import AppContent from './components/AppContent.vue';
import AppNav from './components/AppNav.vue';

export default {
  components: {
    AppNav,
    AppContent
  }
}
</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
