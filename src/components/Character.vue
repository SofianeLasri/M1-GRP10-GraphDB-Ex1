<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  character: {
    id: number;
    name: string;
    image: string;
  };
}>();
</script>

<template>
  <div class="character">
    <img :src="character.image" :alt="character.name" />
    <div class="meta">
      <h2>{{ character.name }}</h2>
    </div>
  </div>
</template>
