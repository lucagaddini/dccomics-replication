<template>
  <div>
    <HeaderComponent />
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

export default {
  components: { HeaderComponent, MainComponent, PreFooterComponent, FooterComponent },
  
}
</script>

<style lang="scss">

</style>
