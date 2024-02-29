<script>
import AppContent from './components/AppContent.vue';
import AppNav from './components/AppNav.vue';
import AppFeature from './components/AppFeature.vue'
import AppFooter from './components/AppFooter.vue';
import AppCTA from './components/AppCTA.vue';

export default {
  components: {
    AppNav,
    AppContent,
    AppFeature,
    AppFooter,
    AppCTA,
  }
}
</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
  <AppFeature></AppFeature>
  <AppFooter></AppFooter>
  <AppCTA></AppCTA>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
