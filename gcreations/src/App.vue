<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import Hero from './components/Hero.vue'
import Cards from './components/Cards.vue'
</script>

<!-- <template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template> -->

<template>
  <header>
    <div class="header-wrapper">
      <Hero />
    </div>
  </header>
  <main>
    <div class="main-wrapper">
      <Cards />
    </div>
  </main>
</template>

<style scoped>
.header-wrapper {
  margin: 0 auto;
  height: auto;
  min-width: 100vw;
  display: flex;
  justify-content: center;
  align-content: center;
}
.main-wrapper {
  margin: 0 auto;
  padding: 20px 40px;
  height: auto;
  width: 100vw;
  
}
</style>
