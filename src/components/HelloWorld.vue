<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
  </div>
</template>

<!-- SCRIPTS -->
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- SCOPED STYLE -->
<style scoped lang="scss">
@import '../assets/style/style.scss';

</style>
