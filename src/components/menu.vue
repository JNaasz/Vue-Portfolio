<template>
    <div class="menu">
        <div v-for="nav in navList"
        :key="nav.id"
        :class="nav.id === active ? 'active' : ''"
        @click="selectMenu"
        >{{ nav.title }}</div>
    </div>
</template>

<script>
// import { sections } from '../content/index.js';
import * as data from '../content/sectionMap.json';
console.log('log this', data.default.Wedding);
const navMap = {
    sections: data.default.Wedding
}

export default {
  name: 'Menu',
  props: {
    navKey: String,
    active: Number
  },
  data: function() {
      return {
          navList: []
      }
  },
  created: function() {
      this.navList = navMap[this.navKey];
      this.active = this.active || 0;
  },    
  methods: {
        selectMenu(event) {
            console.log(event.target);
            //this.active = event.target.innerText;
            //emit event to toggle the inner text of app
        }
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped  lang="scss">
.menu {
  display: flex;
  justify-content: flex-end;

    div {
        margin-left: 10px;
        padding: 8px 10px;
        border: 1px solid purple;

        &.active {
            color: pink;
        }
    }
}
</style>