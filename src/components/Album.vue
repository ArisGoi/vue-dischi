<template>
  <div class="album">
      <img :src="alb.poster" :alt="`${alb} Cover`">
      <h2>{{alb.title}}</h2>
      <p class="autore">{{alb.author}}</p>
      <p class="anno">{{alb.year}}</p>
  </div>
</template>

<!-- SCRIPTS -->
<script>
export default {
  name: 'Album',
  props: {
      alb: Object,
  }
}
</script>

<!-- SCOPED STYLE -->
<style scoped lang="scss">
@import '../assets/style/style.scss';

    .album{
        background-color: $bg-header;
        padding: 15px;
        text-align: center;
        height: 100%;
        overflow: hidden;

        img{
            width: 100%;
        }

        h2{
            margin: 20px 0;
            text-transform: uppercase;
            color: white;
            font-size: 26px;
        }
        p{
            margin: 2px 0;
            color: lightslategray;
            font-size: 20px;
        }
    }
</style>
