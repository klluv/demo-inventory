<template>
    <header>
        <h1 @click="changeTitle">{{ title }}</h1>
    </header>

</template>

<script>
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
        this.title = "12345"
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
