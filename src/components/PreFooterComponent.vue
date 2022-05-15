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

import firstImage from '../assets/img/buy-comics-digital-comics.png';
import secondImage from '../assets/img/buy-comics-merchandise.png';
import thirdImage from '../assets/img/buy-comics-subscriptions.png';
import fourthImage from '../assets/img/buy-comics-shop-locator.png';
import fifthImage from '../assets/img/buy-dc-power-visa.svg';


export default {
  name: 'PreFooterComponent',
  data(){
    return {
        merchLinks: [
          { text:'Digital Comics',
            link:'#',
            icon: firstImage

          },
          { text:'DC Merchandise',
            link:'#',
            icon: secondImage

          },
          { text:'Subscription',
            link:'#',
            icon: thirdImage

          },
          { text:'Comic Shop Locator',
            link:'#',
            icon: fourthImage

          },
          { text:'DC Power Visa',
            link:'#',
            icon: fifthImage

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