<template>
  <main>
    <h3>-- Content goes here --</h3>
  </main>
</template>

<script>
export default {
  name: 'MainComponent'

}
</script>



<style lang="scss">
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
@import '../assets/style/_general.scss';

  main{
    @include flex-cnt();
    height: 300px; // DA TOGLIERE
    background-color: $main-background-color;
    color: white;
  }
</style>