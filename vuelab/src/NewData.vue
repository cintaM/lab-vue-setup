<template>
<!-- <div>
    <h1> {{ greet }} {{ nameG }}</h1>
</div> -->
<div>
    <h1 v-bind:class="!agotado && 'Agotado'">Agotado</h1>
</div>

     <div>     
         <h1 v-for="post in posts" :key="post">
          {{ post.name }} - {{ post.city}} - {{post. studies}}
        </h1>
</div>  
</template>

<script>
export default {
    name: "NewData",
    data(){
        return{
    greet: "Hola",
    nameG: "Cinta",
    agotado: true,

    posts: [{name:"Maria", city: "Madrid", studies: "Universitaria"},{
        name:"Hugo", city: "Sevilla", studies: "ESO"
    }, {name:"Antonio", city: "Valencia", studies: "FP"}]
    }
    }

    }
</script>

<style>
.Agotado{
    display: none;
}
</style>