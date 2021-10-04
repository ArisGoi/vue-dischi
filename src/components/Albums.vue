<template>
  <div class="container-m">
      <div class="albCont" v-for="(album, index) in albumsData" :key="index">
          <Album :alb="album"/>
      </div>
  </div>
</template>

<!-- SCRIPTS -->
<script>
import Album from './Album.vue'
import axios from 'axios';

export default {
  name: 'Albums',
  components: {
      Album
  },
  props: ['opr'],
  data(){
      return{
          albumsData: [],
      }
  },
  created(){
      axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
          this.albumsData = response.data.response;
      });
  }
}
</script>

<!-- SCOPED STYLE -->
<style scoped lang="scss">
@import '../assets/style/style.scss';

.container-m{
    display: flex;
    flex-wrap: wrap;
    padding-top: 40px;

    .albCont{
        width: calc(100% / 5);
        padding: 10px;
    }
}

</style>
