<template>
  <div>
    <HeaderComponent />
    <HeroBannerComponent />
    <MainComponent />
    <PreFooterComponent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import PreFooterComponent from './components/PreFooterComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import HeroBannerComponent from './components/HeroBannerComponent.vue'

export default {
  components: { HeaderComponent, MainComponent, PreFooterComponent, FooterComponent, HeroBannerComponent },
  
}
</script>

<style lang="scss">

</style>
