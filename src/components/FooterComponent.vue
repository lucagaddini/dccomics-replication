<template>
  <footer> 
      <div class="footer_bg_image">
        <div class="footer_top container-lg">
          <div class="col_left">
            <div class="row">

              <div class="col-2 py-5">
                <div class="col_title">Dc Comics</div>
                <ul>
                  <li><a href="#">Characters</a></li>
                  <li><a href="#">Comics</a></li>
                  <li><a href="#">Movies</a></li>
                  <li><a href="#">TV</a></li>
                  <li><a href="#">Games</a></li>
                  <li><a href="#">Videos</a></li>
                  <li><a href="#">News</a></li>
                </ul>

                <div class="col_title">Shop</div>
                <ul>
                  <li><a href="#">Shop DC</a></li>
                  <li><a href="#">Shop Collectibles</a></li>
                </ul>
              </div>

              <div class="col-2 py-5">
                <div class="col_title">Dc</div>
                <ul>
                  <li><a href="#">Terms of use</a></li>
                  <li><a href="#">Privacy Policy (new)</a></li>
                  <li><a href="#">Ad Choices</a></li>
                  <li><a href="#">Advertising</a></li>
                  <li><a href="#">Jobs</a></li>
                  <li><a href="#">Subscriptions</a></li>
                  <li><a href="#">Talent Workshops</a></li>
                  <li><a href="#">CPSC Certificates</a></li>
                  <li><a href="#">Ratings</a></li>
                  <li><a href="#">Shop Help</a></li>
                  <li><a href="#">Contact Us</a></li>
                </ul>
              </div>

              <div class="col-2 py-5">
                <div class="col_title">Sites</div>
                <ul>
                  <li><a href="#">DC</a></li>
                  <li><a href="#">MAD Magazine</a></li>
                  <li><a href="#">DC Kids</a></li>
                  <li><a href="#">DC Universe</a></li>
                  <li><a href="#">DC Power Visa</a></li>
                </ul>
              </div>

            </div>
          </div>
          
        </div>
      </div>

      <div class="footer_bottom container-lg">
        <div class="col_left px-3">
          <button class=sign_up>Sign-Up Now!</button>
        </div>
        <div class="col_right px-3">
          <div class="follow_us_box">
            <span>Follow us</span>
            <div class="social_icons">
              <a v-for="(social,index) in socials" :key="`social-${index}`" :href="social.link"><img :src="social.icon" :alt="social.name"></a>
            </div>

          </div>
        </div>
      </div>

    
  </footer>
</template>

<script>

import firstSocial from '../assets/img/footer-facebook.png';
import secondSocial from '../assets/img/footer-twitter.png';
import thirdSocial from '../assets/img/footer-youtube.png';
import fourthSocial from '../assets/img/footer-pinterest.png';
import fifthSocial from '../assets/img/footer-periscope.png';


export default {
  name: 'FooterComponent',
  data(){
    return{
      socials: [
        {
          name:'Facebook',
          link:'https://www.facebook.com/dc',
          icon: firstSocial

        },
        {
          name:'Twitter',
          link:'https://twitter.com/dccomics',
          icon: secondSocial

        },
        {
          name:'Youtube',
          link:'http://www.youtube.com/user/DCEntertainmentTV',
          icon: thirdSocial

        },
        {
          name:'Pinterest',
          link:'http://www.pinterest.com/dccomics/',
          icon: fourthSocial

        },
        {
          name:'Periscope',
          link:'https://www.periscope.tv/DCComics',
          icon: fifthSocial

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

footer{
  background-color: $footer-bg-color;
  height: 100%;
  width: 100%;
}

.footer_bg_image{
  background-image: url('../assets/img/footer-bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  overflow: hidden;
}

.footer_top{
  @include flex-sbtw();
  color: aliceblue;
  width: 100%;
  height: auto;
  background-image: url(../assets/img/dc-logo-bg.png);
  background-repeat: no-repeat;
  background-position: right center;
  background-size: 50%;

  .col_left{
    width: 100%;
  }
  
  .col_title{
    text-transform: uppercase;
    font-weight: bold;
    color: $footer-col-title;
    padding-bottom: 10px;
  }

  ul{
    list-style: none;
    padding: 0;
    li{
      text-decoration: none;
      a{
        color: $footer-li-color;
        text-decoration: none;
        text-transform: capitalize;
        font-size: 12px;
      }
    }
  }
}

.footer_bottom{
  padding: 35px 0;
  width: 100%;
  height: auto;
  @include flex-sbtw();
  
  .sign_up{
    @include sign-up-btn();
  }

  .follow_us_box{
    @include flex-cnt();

    span{
      color: $primary-color;
      text-transform: uppercase;
      font-size: 25px;
      font-weight:600;
      padding: 0 25px;
    }
    .social_icons a{
      padding: 0 10px;
    }
  }
}

</style>