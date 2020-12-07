<template>
  <div id="app">
    <ul>
      <li @click="changeMenu('one')">one</li>
      <li @click="changeMenu('two')">two</li>
      <li @click="changeMenu('three')">three</li>
    </ul>
    <component :is="current" />
  </div>
</template>

<script>
import One from './One';
import Two from './Two';
import Three from './Three';

export default {
  name: 'Container',
  data() {
    return {
      current: "One"
    }
  },
  components: {
    One,
    Two,
    Three
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
