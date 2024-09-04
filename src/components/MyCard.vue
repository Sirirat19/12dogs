<script>
export default {
  props: ['id', 'name', 'images']
}
</script>

<template>
  <div class="card">
    <div class="image-container">
      <img v-if="images" :src="images" :alt="name">
      <div v-else class="no-image">No Image Available</div>
    </div>
    <div class="container">
      <h4>{{ name }}</h4>
      <p>Architect & Engineer</p>
    </div>
  </div>
</template>

<style scoped>
.card {
  margin: 1rem;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.image-container {
  width: 100%;
  height: 200px; 
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden; 
}

.image-container img {
  width: 100%;
  height: 100%;
  object-fit:scale-down; 
}

.no-image {
  width: 100%;
  height: 100%;
  background-color: #eaeaea;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #888;
}

.container {
  padding: 2px 16px;
}
</style>
