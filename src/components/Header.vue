<template>
  <header>
      <div class="container-l">
          <img class="logo" :src="`${logo}`" alt="Logo Spotify">
          <select v-model="selGenre" @change="$emit('filterSel', selGenre)">
              <option value="">--SELEZIONA UN GENERE--</option>
              <option v-for="genre in genreList" :value="genre" :key="genre">{{genre}}</option>
          </select>
      </div>
  </header>
</template>

<!-- SCRIPTS -->
<script>
export default {
  name: 'Header',
  props: ['logo', 'genreList'],
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
        position: relative;

        .logo{
            height: calc($header-height - 20px);
            margin: 10px 0;
        }

        select{
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            right: 50px;
            height: 25px;
        }
    }
</style>
