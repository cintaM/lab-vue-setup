<template>

<!-- //iteracion 2 -->
<div>
    <h1> {{ greet }} {{ nameG }}</h1>
</div>

<!-- //Iteracion 3 -->
<div>
    <h1 v-if= "agotado === true">Agotado</h1>
</div>
<!-- //iteracion 4 -->
     <div>     
         <h1 v-for="post in posts" :key="post">
          {{ post.name }} - {{ post.city}} - {{post. studies}}
        </h1>
</div>  

<!-- //iteracion 5 -->

<div id="cambiarColor">
          <h1 class="rojo">{{ nameEvent }}</h1>
          <button v-on:click="rojo = 'azul'"> Click me to change the color
          </button>
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
    }, {name:"Antonio", city: "Valencia", studies: "FP"}],
    nameEvent: "Ahora soy de este color",
    }
    }

    }
</script>

<style>


.rojo{
    background-color: blue;
}

.azul{
    background-color: red;
}
</style>