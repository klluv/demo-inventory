<template>
  <div>
    <form-helper>
      <div slot="form-header">
        <h3>Title from the form</h3>
        <p>paragraph from the from</p>
      </div>
      <div slot="form-field">
        <input type="text" placeholder="name" required>
        <input type="password" placeholder="password" required>
      </div>
      <div slot="form-control">
        <button @click="formSubmit">Submit here</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import formHelper from './components/formHelper.vue';

export default {
  components: {
    'form-helper': formHelper
  },
  data() {
      return {
        title: 'title is change'
      }
  },
  methods: {
    
  }
}
</script>

<style>
body{
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

</style>
