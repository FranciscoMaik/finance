<template>
  <div class="body">
    <NavPages />
    <div class="content">
      <TheHeader v-show="showHeader"/>
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'
import NavPages from './components/NavPages.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
    NavPages
  },
  data() {
    return {
      showHeader: true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #f1f1f1;
  display: flex;
  flex-direction: column;
}
.body {
  display: flex;
}
.content {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 24px;
}
</style>
