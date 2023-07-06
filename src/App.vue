<template>
  <div>

    <div id="app">
      <HeaderComp></HeaderComp>
      <button @click="currentTab = nameButton" v-for="nameButton in nameButtons" :key="nameButton.id">
        {{ nameButton }}
      </button>
      <component :is="changeTabs"></component>
      <FooterComp></FooterComp>
    </div>

  </div>
</template>

<script>

import HeaderComp from './components/HeaderComp.vue';
import FooterComp from './components/FooterComp.vue';
import ChangeBedroom from './components/ChangeBedroom.vue';
import ChangeKitchen from './components/ChangeKitchen.vue';
import ChangeBathroom from './components/ChangeBathroom.vue';
import ChangeLivingArea from './components/ChangeLivingArea.vue';


export default {
  name: 'App',
  components: {
    HeaderComp,
    FooterComp,
    ChangeBedroom,
    ChangeKitchen,
    ChangeBathroom,
    ChangeLivingArea
  },
  data() {
    return {
      nameButtons: ['Bathroom', 'Bedroom', 'Kitchen', 'LivingArea'],
      currentTab: 'Bedroom'
    };
  },
  computed: {
    changeTabs() {
      return `Change${this.currentTab}`;
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
