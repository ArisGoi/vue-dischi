<template>
  <div id="app">
    <Header :logo="require('./assets/img/spotify-logo.png')" @search="filterSel"/>
    <main>
      <Albums :opr="filterSel"/>
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
}
</script>

<style lang="scss">
@import './assets/style/style.scss';

</style>
