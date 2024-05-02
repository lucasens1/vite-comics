<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppIcons from './components/AppIcons.vue';
  import AppFooter from './components/AppFooter.vue';
  

  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter,
      AppIcons
    }
  }
</script>

<template>
  <div class = "wrapper">
    <!-- Header -->
    <AppHeader />
    <!-- Main -->
    <AppMain />
    <!-- Icons -->
    <AppIcons />
    <!-- Footer -->
    <AppFooter />

  </div>
</template>

<style lang="scss" scoped>
@import './style/generals.scss';
</style>