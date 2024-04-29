<script setup>
const personagem = defineProps(["name", "id", "image", "location", "gender", "status", "species", "episode"])
</script>

<template> 
    <div class="col-md-3">
        <div class="card p-3 mb-4">
            <img :src=personagem.image>
            <p class="text-center">{{ personagem.name }}</p>
            <p class="text-center">{{ personagem.location }}</p>
            <p class="text-center">{{ personagem.gender }}</p>
            <p class="text-center">{{ personagem.status }}</p>
            <p class="text-center">{{ personagem.species }}</p>
            <p class="text-center">{{ personagem.episode.length }}</p>
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