<template>
  <header>
    <img :src="`${logo}`" alt="Logo Spotify">
  </header>
</template>

<!-- SCRIPTS -->
<script>
export default {
  name: 'Header',
  props: ['logo']
}
</script>

<!-- SCOPED STYLE -->
<style scoped lang="scss">
@import '../assets/style/style.scss';

</style>
