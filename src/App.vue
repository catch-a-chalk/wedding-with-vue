<template>
  <div>
    <app-layout/>
    <home-view/>
  </div>
</template>

<script>
import AppLayout from './layouts/AppLayout.vue'
import HomeView from './components/HomeView.vue'

export default {
  name: 'App',
  components: {
    AppLayout,
    HomeView
  }
}
</script>

<style lang="scss">
@import "./assets/scss/app.scss";
</style>
