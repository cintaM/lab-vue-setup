<template>
<!-- <div>
    <h1> {{ greet }} {{ nameG }}</h1>
</div> -->
<div>
    <h1 v-bind:class="!agotado && 'Agotado'">Agotado</h1>
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
    }
    }

    }
</script>

<style>
.Agotado{
    display: none;
}
</style>