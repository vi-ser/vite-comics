<script>
import AppContent from './components/AppContent.vue';
import AppNav from './components/AppNav.vue';
import AppIconSection from './components/AppIconSection.vue'

export default {
  components: {
    AppNav,
    AppContent,
    AppIconSection,
  }
}
</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
  <AppIconSection></AppIconSection>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
