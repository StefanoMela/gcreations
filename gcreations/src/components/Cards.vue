<script setup lang="ts">
import { ref } from 'vue'

// Fake data per il carousel
const items = ref([
  { img: 'https://picsum.photos/300/200', title: 'Card 1', description: 'Description for card 1' },
  { img: 'https://picsum.photos/300/200', title: 'Card 2', description: 'Description for card 2' },
  { img: 'https://picsum.photos/300/200', title: 'Card 3', description: 'Description for card 3' },
  { img: 'https://picsum.photos/300/200', title: 'Card 4', description: 'Description for card 4' },
  { img: 'https://picsum.photos/300/200', title: 'Card 5', description: 'Description for card 5' },
])

// Indice attuale
const currentIndex = ref(0)

// Funzioni per navigare
const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + items.value.length) % items.value.length
}

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % items.value.length
}
</script>

<template>
  <div class="carousel">
    <div class="carousel-wrapper">
      <!-- Visualizza solo l'elemento corrente -->
      <div
        v-for="(item, index) in items"
        :key="index"
        class="carousel-item"
        :class="{ active: index === currentIndex }"
      >
        <img :src="item.img" :alt="item.title"  class="carousel-img"/>
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
      </div>
    </div>
    <!-- Pulsanti di navigazione -->
    <button @click="prevSlide" class="prev-btn">‹</button>
    <button @click="nextSlide" class="next-btn">›</button>
  </div>
</template>

<style scoped>
.carousel {
  position: relative;
  width: 80%;
  margin: auto;
  overflow: hidden;
}

.carousel-wrapper {
  display: flex;
  transition: transform 0.5s ease-in-out;
  width: 100%;
  align-content: center;
}

.carousel-item {
  flex: 0 0 100%;
  text-align: center;
  display: none;
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
  background-color: blue;
  padding: 24px 0;
}

.carousel-item img {
  max-width: 100%;
  height: auto;
  border-radius: 8px;

}

.carousel-item.active {
  display: block;
  opacity: 1;
}

.prev-btn,
.next-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  cursor: pointer;
  z-index: 10;
}

.prev-btn {
  left: 10px;
}

.next-btn {
  right: 10px;
}

.prev-btn:hover,
.next-btn:hover {
  background-color: rgba(0, 0, 0, 0.8);
}
</style>
