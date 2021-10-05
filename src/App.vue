<template>
  <div id="app">
    <Header :logo="require('./assets/img/spotify-logo.png')" @filterSel="filterMet" :genreList="genreList"/>
    <main>
      <Albums :opr="filterExp" @genreList="genreListEvent"/>
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
    return{
      filterExp: "",
      genreList: []
    }
  },
  methods:{
    filterMet(filterSel){
      this.filterExp = filterSel;
      console.log(this.filterExp);
    },
    genreListEvent(list) {
      this.genreList = list;
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/style.scss';

</style>
