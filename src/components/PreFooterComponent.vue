<template>
  <section class="section_bg">
    <div class="card_container container-lg"> 
      <div class="card_box">
        <a href="#">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comics">
          <span>Digital Comics</span>
        </a>
      </div>

      <div class="card_box">
        <a href="#">
          <img src="../assets/img/buy-comics-merchandise.png" alt="DC Merchandise">
          <span>DC Merchandise</span>
        </a>
      </div>

      <div class="card_box">
        <a href="#">
          <img src="../assets/img/buy-comics-subscriptions.png" alt="Subscription">
          <span>Subscription</span>
        </a>
      </div>

      <div class="card_box">
        <a href="#">
          <img src="../assets/img/buy-comics-shop-locator.png" alt="Comic Shop Locator">
          <span>Comic Shop Locator</span>
        </a>
      </div>

      <div class="card_box">
        <a href="#">
          <img src="../assets/img/buy-dc-power-visa.svg" alt="DC Power Visa">
          <span>DC Power Visa</span>
        </a>
      </div>


    </div>
  </section>
</template>

<script>
export default {
  name: 'PreFooterComponent'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
@import '../assets/style/_general.scss';

.section_bg{
  @include flex-cnt();
  background-color: $primary-color;
  height: 150px
}

.card_container{
  @include flex-sbtw();

  .card_box{
    @include flex-sbtw();

    a{
      @include flex-cnt();
      flex-wrap: wrap;
      color: white;
      text-decoration: none;
      text-transform: uppercase;
      span{
        padding: 10px 25px;
      }

      img{
        width: 50px;
        height: auto;
      }
    }
  
  }
}



</style>