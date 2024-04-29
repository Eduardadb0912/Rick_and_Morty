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
body{
    background-color: rgb(169, 211, 233);
}
.col-md-3 {
    background-color: rgb(169, 211, 233);
}
</style>
