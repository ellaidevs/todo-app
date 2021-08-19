<template>
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
</template>

<script>
import Background from './Background.vue'
import Icon from './Icon.vue'

export default {
  data() {
    return {
      theme: true,
    }
  },
  components: {
    Background,
    Icon,
  },
  methods: {
    toggleTheme() {
      this.theme = !this.theme
    },
  },
}
</script>

<style scoped>
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
}
</style>
