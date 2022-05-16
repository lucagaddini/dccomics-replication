<template>
  <section class="jumbotron">
    <img src="https://guidatv.sky.it/uuid/3e779445-c434-4d5d-9ef3-71ac4799a87e/16-9?md5ChecksumParam=b86cd899991a006dfe75d9aac8990f16&tr=n-scene_128" alt="">
  </section>
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
  @include flex-cnt();
  overflow: hidden;
}


</style>