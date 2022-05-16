<template>
  <main>
    <div class="container">
      <div class="title_box">Current Series</div>
      <div class="container_card">
        <ComicsCardComponent 
        v-for="(item,index) in ComicsArray"
        :key="`item-${index}`"
        :cardItem = "item" />
      </div>
      <div class="load_more_container">
        <button class="btn_load_more">Load More</button>
      </div>
    </div>
  </main>
</template>

<script>
import ComicsCardComponent from './ComicsCardComponent.vue';
import ComicsList from '../assets/data/dc-comics';

export default {
    name: "MainComponent",
    components: { ComicsCardComponent },
    data() {
      return {
        ComicsArray: ComicsList
      }
    }

}
</script>



<style lang="scss">
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
@import '../assets/style/_general.scss';

  main{
    @include flex-cnt();
    height: 100%;
    width: 100%;
    background-color: $main-background-color;
    color: white;
    position: relative;

    .title_box{
      font-size: 25px;
      position: absolute;
      top: -25px;
      left: 10%;
      margin: 0;
      padding: 10px 25px 8px 25px;
      line-height: 0.9;
      color: #fff;
      background-color: $primary-color;
      text-transform: uppercase;
      font-weight: 600;
    }

    .container_card{
      @include flex-start();
      margin-top: 25px;
    }

    .load_more_container{
      @include flex-cnt();
      padding: 50px;
    }

    .btn_load_more {
      background-color: $primary-color;
      color: #ffffff;
      border: 2px solid $primary-color;
      padding: 10px 35px;
      text-transform: uppercase;
    }

  }
</style>