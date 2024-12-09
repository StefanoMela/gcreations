<script setup lang="ts"></script>

<template>
  <div class="hero-container">
    <div class="layer"></div>
    <div class="row">
      <div class="col 1">
        <div class="img-container">
          <img src="/hero1.jpg" alt="" />
        </div>
      </div>
      <div class="col 2">
        <div class="img-container">
          <img src="/hero2.jpg" alt="" />
        </div>
      </div>
      <div class="col 3">
        <div class="img-container">
          <img src="/hero3.jpg" alt="" />
        </div>
      </div>
    </div>
    <h1>G Creations</h1>
    <h5>Handmade crafts made with love in Sardinia</h5>
  </div>
</template>

<style scoped>
/* GENERAL */
.hero-container {
  height: 80vh;
  width: 100%;
  padding: 20px 40px;
  color: rgb(13, 38, 79);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  margin-bottom: 48px;
  position: relative;
}
.hero-container > h1 {
  font-size: 48px;
  letter-spacing: 0.2rem;
  font-weight: 600;
}
.hero-container > h5 {
  font-size: 32px;
  letter-spacing: 2px;
}

/* LAYER */
/* 
.layer {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 80%;
  background-color: rgba(172, 113, 113, 0.5);
  backdrop-filter: blur(80%);
  z-index: -1;
} */

/* HERO CARDS */

.row {
  display: flex;
  justify-content: end;
  gap: 12px;
  z-index: -1;
}
.col:nth-child(even) {
  margin-top: 0;
}
.col:nth-child(odd) {
  margin-top: -48px;
}

.img-container {
  width: 360px;
}

.img-container > img {
  width: 100%;
  height: 480px;
  object-fit: cover;
  border-radius: 12px;
}
</style>
