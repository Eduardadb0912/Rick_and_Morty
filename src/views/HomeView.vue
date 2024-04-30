<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListRick from '../components/ListRickMorty.vue';

let personagens = reactive(ref())

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character/?limit=20&offset=0")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  })
})

</script>

<template>
  <main style="background: linear-gradient(to bottom, #6be0e9, #d9f344)">
    <div class="container">
            <div class="card-body mt-4 mb-8 row" style="padding: 0;">
              <ListRick 
                v-for="personagem in personagens" 
                :key="personagem.id" 
                :name="personagem.name"
                :image="personagem.image"
                :species="personagem.species"
                :status="personagem.status"
                :gender="personagem.gender"
                :location="personagem.location.name"
                :episode = "personagem.episode"
              />
            </div>
          </div>
  </main>
</template>

