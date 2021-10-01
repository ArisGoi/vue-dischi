<template>
  <div>
      <Album/>
  </div>
</template>

<!-- SCRIPTS -->
<script>
import Album from './Album.vue'

export default {
  name: 'Albums',
  components: {
      Album
  }
}
</script>

<!-- SCOPED STYLE -->
<style scoped lang="scss">
@import '../assets/style/style.scss';

</style>
