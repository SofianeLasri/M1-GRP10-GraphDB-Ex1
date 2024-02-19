<script setup lang="ts">
import RickAndMorty from "@/components/icons/RickAndMorty.vue";
import Character from "@/components/Character.vue";

const characters = [];

for (let i = 1; i < 21; i++) {
  characters.push({
    id: i,
    name: `Character ${i}`,
    image: `https://rickandmortyapi.com/api/character/avatar/${i}.jpeg`
  });
}
</script>

<template>
  <div class="home">
    <div class="header">
      <h1>Rick and Morty characters</h1>
      <div class="hero-image">
        <RickAndMorty />
      </div>
    </div>
    <div class="content">
      <div class="list">
        <Character v-for="character in characters" :key="character.id" :character="character" />
      </div>
      <div class="pagination">
        <button v-for="i in 42" :key="i" class="page">
          {{ i }}
        </button>
      </div>
    </div>
  </div>
</template>
