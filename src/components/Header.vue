<template>
    <header>
        <h1 @click="changeTitle">{{ title }}</h1>
    </header>

</template>

<script>
import { bus } from '../main';
export default {
    props: {
        title: {
            type: String
        }
    },
  data () {
      return {
       title: 'vuejs has begin'
      }
  },
  methods: {
    changeTitle: function() {
        // this.$emit('changeTitle', 'Vue title Changed');
        this.title = 'Vue Changed'
        bus.$emit('titleChanger', 'Vue Changed')
    }
  }
}
</script>

<style scoped>
header{
    background: lightblue;
    padding:10px;
}
h1{
    color: #222;
    text-align: center;
    
}


</style>
