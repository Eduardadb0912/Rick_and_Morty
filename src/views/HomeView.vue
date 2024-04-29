<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListRick from '../components/List_Rick_and_Morty.vue';

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
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-12">
          <div class="card">
            <div class="card-body row" style="padding: 0;">
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
        </div>
      </div>
    </div>
  </main>
</template>
