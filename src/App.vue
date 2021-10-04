<template>
  <div id="app">
    <Header :logo="require('./assets/img/spotify-logo.png')" @filterSel="filterMet"/>
    <main>
      <Albums :opr="filterExp"/>
    </main>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Albums from './components/Albums.vue'

export default {
  name: 'App',
  components: {
    Header,
    Albums,
  },
  data() {
    return{ // Ho fixato la variabile
      filterExp: ""
    }
  },
  methods:{
    filterMet(filterSel){
      this.filterExp = filterSel;
      console.log(this.filterExp);
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/style.scss';

</style>
