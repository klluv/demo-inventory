<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <app-kaka v-bind:kakas="kakas"></app-kaka>
    <app-footer v-bind:copyright="copyright"></app-footer>
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
        kakas: [
                {name: 'Sukri', speciality: 'Vue Components', show: false},
                {name: 'Seno', speciality: 'HTML Wizardry', show: false},
                {name: 'Rope', speciality: 'Click Events', show: false},
                {name: 'Bonar', speciality: 'Conditionals', show: false},
                {name: 'Luci', speciality: 'Webpack', show: false},
                {name: 'Jess', speciality: 'Data Diggin', show: false}
            ],
            title: "Vue Kaka"
      }
  }
}
</script>

<style>



</style>
