<script>
import AppContent from './components/AppContent.vue';
import AppNav from './components/AppNav.vue';
import AppIconSection from './components/AppIconSection.vue'
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppContent,
    AppIconSection,
    AppFooter,
  }
}
</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
  <AppIconSection></AppIconSection>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
