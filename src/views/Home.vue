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
// import @url('https://fonts.googleapis.com/css?family=Roboto+Condensed');

export default {
  name: 'Home',
  components: {
    Header,
    List,
  },
}
</script>
