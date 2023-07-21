<template>
    <div id="add-blog">
        <h2>Menambah blog baru</h2>
        <form>
            <label>Judul blog: </label>
            <input type="text" v-model.trim="blog.title" required />
            <label>Konten blog: </label>
            <textarea v-model="blog.content" ></textarea>
            <div id="checkbox">
                <label>Sukri</label>
                <input type="checkbox" value="Sukri" v-model="blog.categories" >
                <label>Bonar</label>
                <input type="checkbox" value="Bonar" v-model="blog.categories" >
                <label>Rope</label>
                <input type="checkbox" value="Rope" v-model="blog.categories" >
                <label>Ryzen</label>
                <input type="checkbox" value="Ryzen" v-model="blog.categories" >
            </div>
            <label>Author: </label>
            <select v-model="blog.author">
                <option v-for="author in authors">{{ author }}</option>
            </select>
        </form>
        <div id="preview">
            <h3>Preview blog</h3>
            <p>Judul Blog: {{ blog.title }}</p>
            <p>Konten Blog: </p>
            <p>{{ blog.content }} </p>
            <p>Kategori Blog: </p>
            <ul>
                <li v-for="kategori in blog.categories">{{ kategori }}</li>
            </ul>
            <p>author: {{ blog.author }}</p>
        </div>
    </div>
</template>

<script>


export default {
    data() {
        return {
            blog: {
                title: '',
                content:'',
                categories: [],
                author: ''
            },
            authors:['Sukri Stankovic','Naga Bonar','Rope Villian']
        }
    },
    methods: {

    }
}
</script>

<style>
#add-blog *{
    box-sizing: border-box;
}
#add-blog{
    margin: 20px auto;
    max-width: 500px;
}
label{
    display: block;
    margin: 20px 0 10px;
}
input[type="text"], textarea{
    display: block;
    width: 100%;
    padding: 8px;
}
#preview{
    padding: 10px 20px;
    border: 1px dotted #ccc;
    margin: 30px 0;
}
h2{
    margin-top: 10px;
}
#checkbox input{
    display: inline-block;
    margin-right: 8px;
}
#checkbox label{
    display: inline-block;

}
</style>
