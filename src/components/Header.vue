<template>
  <header>
      <div class="container-l">
          <img class="logo" :src="`${logo}`" alt="Logo Spotify">
          <select v-model="selGenre" @change="$emit('filterSel', selGenre)">
              <option value="">all</option>
              <option value="rock">rock</option>
              <option value="jazz">jazz</option>
              <option value="pop">pop</option>
          </select>
      </div>
  </header>
</template>

<!-- SCRIPTS -->
<script>
export default {
  name: 'Header',
  props: ['logo'],
  data(){
      return {
          selGenre:"all",
      }
  }
}
</script>

<!-- SCOPED STYLE -->
<style scoped lang="scss">
@import '../assets/style/style.scss';

    header{
        height: $header-height;
        background-color: $bg-header;

        .logo{
            height: calc($header-height - 20px);
            margin: 10px 0;
        }
    }
</style>
