<template>
  <main>
    <div class="container">
      <div class="title_box">Current Series</div>
    </div>
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
    position: relative;

    .title_box{
      font-size: 25px;
      position: absolute;
      top: -25px;
      left: 230px;
      margin: 0;
      padding-top: 10px;
      padding-right: 25px;
      padding-bottom: 8px;
      padding-left: 25px;
      line-height: 0.9;
      color: #fff;
      background-color: $primary-color;
      text-transform: uppercase;
      font-weight: 600;
    }
  }
</style>