<template>
  <header>
      <div class="container-l">
          <img class="logo" :src="`${logo}`" alt="Logo Spotify">
      </div>
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

    header{
        height: $header-height;
        background-color: $bg-header;

        .logo{
            height: calc($header-height - 20px);
            margin: 10px 0;
        }
    }
</style>
