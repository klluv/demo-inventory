<template>
    <div>
        <form-helper>
            <div slot="form-header">
                <h3>Kritik dan saran</h3>
                <p>Isikan form ini untuk menjadi pertimbangan kami</p>
            </div>
            <div slot="form-field">
                <input type="text" placeholder="nama" required />
                <label>Pesan:</label>
                <textarea></textarea>
            </div>
            <div slot="form-control">
                <button v-on:click="handleSubmit">Kirim</button>
            </div>
        </form-helper>
    </div>
</template>

<script>
// Imports
import formHelper from './formHelper.vue'

export default {
    components: {
        'form-helper': formHelper
    },
    data () {
        return {

        }
    },
    methods: {
        handleSubmit: function(){
            alert('thanks for submitting form one & contacting us');
        }
    }
}
</script>

<style>
body{
    margin: 0;
    font-family: 'Nunito SemiBold';
}
</style>