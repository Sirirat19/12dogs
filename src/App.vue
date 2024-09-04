<script setup>
import Navbar from './components/MyNavbar.vue';
import Card from './components/MyCard.vue';
import content from './content.json';
import Header from './components/Header.vue';
</script>

<template>
  <Navbar />
  <Header />
  <div className="grid-container">
    <Card
      v-for="item in content"
      :key="item.id"
      :id="item.id"
      :name="item.name"
      :images="item.images"
    />
  </div>
</template>

<style scoped>
  .grid-container {
    display: grid;
    grid-column-gap: 0.5rem;
    grid-row-gap: 0.5rem;
  }
  @media (min-width: 576px) {
    .grid-container{grid-template-columns: repeat(1,1fr);}
  }
  @media (min-width: 992px) {
    .grid-container{grid-template-columns: repeat(3,1fr);}
  }
</style>
