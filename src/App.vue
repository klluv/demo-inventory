<template>
  <div>
    <app-header></app-header>
    <app-kaka></app-kaka>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';  
import Kaka from './components/Kaka.vue';   

export default {
  components: {
    'app-header':Header,
    'app-footer':Footer,
    'app-kaka':Kaka
  },
  data () {
      return {
       
      }
  }
}
</script>

<style>



</style>