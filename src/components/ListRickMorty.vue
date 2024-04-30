<script setup>
const personagem = defineProps(["name", "id", "image", "location", "gender", "status", "species", "episode"])
</script>

<template> 
    <div class="col-md-3 d-flex">
            <div class="card p-3 mb-4">
            <img :src=personagem.image>
            <p class="text-center"><strong>NAME: </strong> {{ personagem.name }}</p>
            <p class="text-center"><strong>LOCAL: </strong>{{ personagem.location }}</p>
            <p class="text-center"><strong>GENDER: </strong>{{ personagem.gender }}</p>
            <p class="text-center"><strong>STATUS: </strong>{{ personagem.status }}</p>
            <p class="text-center"><strong>SPECIES: </strong>{{ personagem.species }}</p>
            <p class="text-center"><strong>EPISODE: </strong>{{ personagem.episode.length }}</p>
        </div>
    </div>
</template>

<style>

body.pagina-b {
  background: linear-gradient(to bottom, #6be0e9, #d9f344); /* Gradiente de fundo para a página B */
}

.col-md-3 {
    background-color: rgba(107, 225, 233, 0);
}
/* body{
    background-color: rgb(169, 211, 233);
}
.col-md-3 {
    background-color: rgb(168, 211, 233);
} */

.card{
    background-color:  rgb(149, 255, 0);
    
}

.text-center{
    color: rgb(43, 150, 20);
}
</style>