<template>
  <header class="container">

    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="DC Logo">
    </div>

    <nav>
      <ul>
        <li class="active"><a href="#">Link 1 </a></li>
        <li><a href="#">Link 2</a></li>
        <li><a href="#">Link 3</a></li>
        <li><a href="#">Link 4</a></li>
      </ul>
    </nav>

  </header>
</template>

<script>
export default {
  name: 'HeaderComponent'

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
  //line-height: 150px;

  nav ul{
    @include flex-cnt();
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