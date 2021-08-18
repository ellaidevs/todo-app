<template>
  <div class="home">
    <div>
      <Background :theme="theme" />
      <header>
        <h1>TODO</h1>
        <div>
          <Icon @click="toggleTheme" :icon="theme" />
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
</style>
