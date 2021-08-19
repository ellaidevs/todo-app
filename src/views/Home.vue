<template>
  <div class="home">
    <div>
      <Header />
      <List />
      <!-- <footer>Drag and drop to reorder list</footer> -->
    </div>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import List from '../components/List.vue'

export default {
  name: 'Home',
  components: {
    Header,
    List,
  },
}
</script>

<style>
body {
  background: hsl(235, 21%, 11%);
  font-size: 18px;
  color: white;
}
</style>
