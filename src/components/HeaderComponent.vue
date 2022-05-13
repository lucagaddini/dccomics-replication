<template>
  <header class="container">

    <div class="logo">
      <a href="#"><img src="../assets/img/dc-logo.png" alt="DC Logo"></a>
    </div>

    <nav>
      <ul>
        <li 
          v-for="(item,index) in menuItems" 
          :key="`menu-${index}`"
          :class="{'active' : item.isActive}"
        ><a :href="item.link">{{item.name}}</a>
        </li>
      </ul>
    </nav>

  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data(){
    return{

      menuItems: [
        {
          name: 'Characters',
          link: '#',
          isActive: false
        },
        {
          name: 'Comics',
          link: '#',
          isActive: true
        },
        {
          name: 'Movies',
          link: '#',
          isActive: false
        },
        {
          name: 'TV',
          link: '#',
          isActive: false
        },
        {
          name: 'Games',
          link: '#',
          isActive: false
        },
        {
          name: 'Collectibles',
          link: '#',
          isActive: false
        },
        {
          name: 'Videos',
          link: '#',
          isActive: false
        },
        {
          name: 'Fans',
          link: '#',
          isActive: false
        },
        {
          name: 'News',
          link: '#',
          isActive: false
        },
        {
          name: 'Shop',
          link: '#',
          isActive: false
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

header{
  @include flex-sbtw();
  padding: 25px;
  height: 150px;
  width: 100%;
  //line-height: 150px;

  nav ul{
    @include flex-cnt();
    width: 100%;
    list-style: none;
    
    li{
      padding: 15px;
      line-height: 136px;
      
      &:hover,
      &.active{
          box-shadow: inset 0 -5px 0 $primary-color;
      }
      &.active a{
          color: $primary-color;
      }

      a {
        text-decoration: none;
        color: $nav-bar-text-color;
        text-transform: uppercase;
        font-weight:600;
        &:hover{
          color: $primary-color;
        }
      }
    }

  }
}

</style>