<template>
  <div class="home">
    <div>
      <img :src="backgroundImg" alt="desktop-dark" class="background-img" />
      <header>
        <h1>TODO</h1>
        <div>
          <Icon icon="check" />
        </div>
      </header>
    </div>
  </div>
</template>

<script>
import desktopDark from '../assets/images/bg-desktop-dark.jpg'
import Icon from '../components/Icon.vue'

export default {
  name: 'Home',
  data() {
    return {
      backgroundImg: desktopDark,
    }
  },
  components: {
    Icon,
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
body {
  background: hsl(235, 21%, 11%);
}

h1 {
  color: white;
}
</style>
