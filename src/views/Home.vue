<template>
  <div class="home">
    <div>
      <Background :theme="theme" />
      <header>
        <div class="header">
          <div class="title">
            <h1>TODO</h1>
          </div>
          <div class="icon">
            <Icon @click="toggleTheme" :icon="theme" />
          </div>
        </div>
      </header>
    </div>
  </div>
</template>

<script>
import Background from '../components/Background.vue'
import Icon from '../components/Icon.vue'

export default {
  name: 'Home',
  data() {
    return {
      theme: true,
    }
  },
  methods: {
    toggleTheme() {
      this.theme = !this.theme
    },
  },
  components: {
    Background,
    Icon,
  },
}
</script>

<style>
body {
  background: hsl(235, 21%, 11%);
}

h1 {
  color: white;
}

.header {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-auto-rows: minmax(100px, auto);
}

h1 {
  margin: 0;
  padding: 0;
}
.title,
.icon {
  margin: 50px auto;
  /* border: 1px solid white; */
}
</style>
