<template>
  <div id="app">
    <Menu class="main-menu" navKey="sections" :active=99></menu>

    <div id="content"></div>

    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Menu from './components/menu.vue';
// import { sections } from './content/index.js';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Menu
  },
  methods: {
    getNavList: function() {
      // console.log('sectionssss', sections);
      // return sections;
      return '';
    }
  },
  computed: {
    navList: function () {
      // console.log('sectionssss', sections);
      // return sections;
      return '';
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
