<template>
    <div id="kaka">
        <ul>
            <li v-for="kaka in kakas" @click="kaka.show = !kaka.show">
            <h2>{{ kaka.name }}</h2>
            <h3 v-show="kaka.show">{{ kaka.speciality }}</h3>
            </li>
        </ul>
    </div>
</template>
  
  <script>
  
  export default {
    data () {
        return {
            kakas: [
                {name: 'Sukri', speciality: 'Vue Components', show: false},
                {name: 'Seno', speciality: 'HTML Wizardry', show: false},
                {name: 'Rope', speciality: 'Click Events', show: false},
                {name: 'Bonar', speciality: 'Conditionals', show: false},
                {name: 'Luci', speciality: 'Webpack', show: false},
                {name: 'Jess', speciality: 'Data Diggin', show: false}
            ]
        }
    }
  }
  </script>
  
  <style scoped>
  #kakas{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
}

  </style>