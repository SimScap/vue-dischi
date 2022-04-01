<template>
<div class="container-fluid text-center  p-5">
    <div class="row ">
    <div class="col-12 d-flex flex-wrap ">
    <div class="card p-3 m-2" v-for="element in singersList " :key="element.index">
    <img :src="element.poster" class="card-img-top" alt="element.poster">
    <div class="card-body">
        <h5 class="card-title">{{element.title}}</h5>
        <p class="card-text">{{element.author}}</p>
        <p class="card-text">{{element.year}}</p>
    </div>
    </div>
</div>
</div>
</div>
</template>

<script>
import axios from "axios";

export default {
name: 'mainContent',
data: function(){
    return{
    singersList : null,
    }
},
created: function(){
    this.getApiList();
},
methods:{
    getApiList(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((result) =>{
        this.singersList = result.data.response;
        console.table(this.singersList);
    })
    .catch((error) =>{
        console.error(error)
    })
    }    
}}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.row{
    border: 2px solid purple;
}
div.container-fluid{
background-color: rgb(77, 115, 153);
height:calc(100vh - 100px);
overflow-y: auto;
}
.card{
    width: 200px;
    background-color: lightgrey;
}
</style>
