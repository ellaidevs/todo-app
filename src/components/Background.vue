<template>
  <img
    v-if="theme === true"
    :src="backgroundDark"
    alt="desktop-dark"
    class="background-img"
  />
  <img
    v-else
    :src="backgroundLight"
    alt="desktop-dark"
    class="background-img"
  />
</template>

<script>
import backgroundDark from '../assets/images/bg-desktop-dark.jpg'
import backgroundLight from '../assets/images/bg-desktop-light.jpg'
export default {
  name: 'Background',
  props: ['theme'],
  data() {
    return {
      backgroundDark: backgroundDark,
      backgroundLight: backgroundLight,
    }
  },
}
</script>

<style>
.background-img {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
</style>
