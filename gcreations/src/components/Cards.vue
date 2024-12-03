<script setup lang="ts">
import { ref } from 'vue'

defineProps<{
  img: string
  title: string
  description: string
}>()

const emit = defineEmits(['click'])

// Fake data per 8 card
const cards = ref([
  { img: 'https://placehold.co/300x200', title: 'Card 1', description: 'Description for card 1' },
  { img: 'https://placehold.co/300x200', title: 'Card 2', description: 'Description for card 2' },
  { img: 'https://placehold.co/300x200', title: 'Card 3', description: 'Description for card 3' },
  { img: 'https://placehold.co/300x200', title: 'Card 4', description: 'Description for card 4' },
  { img: 'https://placehold.co/300x200', title: 'Card 5', description: 'Description for card 5' },
  { img: 'https://placehold.co/300x200', title: 'Card 6', description: 'Description for card 6' },
  { img: 'https://placehold.co/300x200', title: 'Card 7', description: 'Description for card 7' },
  { img: 'https://placehold.co/300x200', title: 'Card 8', description: 'Description for card 8' },
])
</script>

<template>
  <div class="cards">
    <!-- Ciclo attraverso i dati e creo una card per ogni elemento -->
    <div v-for="(card, index) in cards" :key="index" class="card">
      <img :src="card.img" :alt="card.title" />
      <h3>{{ card.title }}</h3>
      <p>{{ card.description }}</p>
    </div>
  </div>
</template>

<style scoped>
.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
.card {
  border: 1px solid #ccc;
  padding: 20px;
  background-color: #ccc;
  cursor: pointer;
}
.card:hover{
  background-color: #aaa;
  
}
</style>
