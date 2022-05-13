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
    height: 500px; // DA TOGLIERE
    width: 100%;
    background-color: $main-background-color;
    color: white;
    
  }
</style>