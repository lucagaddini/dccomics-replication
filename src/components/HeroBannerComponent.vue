<template>
  <section class="jumbotron"></section>
</template>

<script>
export default {
  name: 'HeroBannerComponent'
}
</script>

<style lang="scss" scoped>

@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
@import '../assets/style/_general.scss';

.jumbotron{
  height: 400px;
  @include flex-start();
  overflow: hidden;
  background-image: url('../assets/img/jumbotron.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}

</style>