<template>
  <div id="app">
    <ul>
      <li @click="changeMenu('dynamic')">dynamic</li>
      <li @click="changeMenu('recursive')">recursive</li>
      <li @click="changeMenu('three')">three</li>
    </ul>
    <component :is="current" />
  </div>
</template>

<script>
import Dynamic from './components/Dynamic/Dynamic'
import Recursive from './components/Recursive/Recursive'

export default {
  name: 'App',
  data() {
    return {
      current: "dynamic"
    }
  },
  components: {
    Dynamic,
    Recursive
  },
  methods: {
    changeMenu(menu) {
      this.current = menu;
    }
  }
};
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
