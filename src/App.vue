<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';

  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
    }
  }
</script>

<template>
  <div class = "wrapper">
    <!-- Header -->
    <AppHeader />
    <!-- Main -->
    <AppMain />
    <!-- Footer -->
    <AppFooter />
  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  width : 100%;
  margin : 0 auto;
}
</style>