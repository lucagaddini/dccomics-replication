<template>
  <div class="card">
    <div class="image_container">
      <img :src="cardItem.thumb" :alt="cardItem.series">
      <div class="info_layer">
        <div>
          <span>Price: </span>
          <span>{{cardItem.price}}</span>
        </div>

        <div>
          <span>Type: </span>
          <span>{{cardItem.type}}</span>
        </div>
      
      </div>
    </div>
    <h5>{{cardItem.series}}</h5>
  </div>
</template>

<script>
export default {
  name: 'ComicsCardComponent',
  props : {
    cardItem: Object
  }
}
</script>

<style lang="scss">
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
@import '../assets/style/_general.scss';

.card{
  @include flex-column-start();
  width: calc(100%/6 - 2rem);
  height: 100%;
  margin: 1rem;
  background-color: transparent;

  &:hover .image_container .info_layer{
    display: flex;
  }

  &:hover h5{
    text-decoration: underline;
    color: $primary-color;
  }

  .image_container{
    width: 100%;
    height: 180px;
    overflow: hidden;
    cursor: pointer;
    position: relative;

    img{
      width: 100%;
    }
    
    .info_layer{
      @include flex-column-cnt();
      display: none;
      position: absolute;
      top:0;
      left:0;
      width: 100%;
      height: 180px;
      background-color: rgba($color: $primary-color, $alpha: .8);
      color: white;
    }

    
  }

  h5{
    padding-top: 10px;
    text-transform: uppercase;
    font-size: 15px;
  }
}

</style>