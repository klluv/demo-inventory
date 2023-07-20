<template>
    <footer>
        <p>{{ copyright }} {{ title }}</p>
    </footer>
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
         copyright:'Copyright 2023 Vue KAKA'
        }
    },
    created(){
      bus.$on('titleChanger', (data) => {
        this.title = data;
      })
    }
  }
  </script>
  
  <style scoped>
footer{
    background: #222;
    padding: 6px;
}
p{
    color:lightblue;
    text-align: center;
}
  
  </style>
