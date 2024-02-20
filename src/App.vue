<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <hello-world msg="Welcome to Your Vue.js App"/>
    <testing-component />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TestingComponent from './components/TestingComponent.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TestingComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
