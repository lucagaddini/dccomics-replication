<template>
  <section class="section_bg">
    <div class="card_container container-lg"> 

      <div v-for="(merchLink,index) in merchLinks" :key="`merchMenu-${index}`" class="card_box">
        <a :href="merchLink.link">
          <img :src="merchLink.icon" :alt="merchLink.text">
          <span>{{merchLink.text}}</span>
        </a>
      </div>

    </div>
  </section>
</template>

<script>

export default {
  name: 'PreFooterComponent',
  data(){
    return {
        merchLinks: [
          { text:'Digital Comics',
            link:'#',
            icon: require ('../assets/img/buy-comics-digital-comics.png')

          },
          { text:'DC Merchandise',
            link:'#',
            icon: require ('../assets/img/buy-comics-merchandise.png')

          },
          { text:'Subscription',
            link:'#',
            icon: require ('../assets/img/buy-comics-subscriptions.png')

          },
          { text:'Comic Shop Locator',
            link:'#',
            icon: require ('../assets/img/buy-comics-shop-locator.png')

          },
          { text:'DC Power Visa',
            link:'#',
            icon: require ('../assets/img/buy-dc-power-visa.svg')

          },
        ]
    }
  }
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