<template>
  <div class="input-container">
    <input type="checkbox" />
    <input type="text" placeholder="Create a new todo..." />
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.input-container {
  border-radius: 5px;
  background: hsl(235, 24%, 19%);
  max-width: 400px;
  /* to arrange the todo title length, check the container max-width above */
  margin: 0 auto;
}

input[type='checkbox'] {
  padding: 10px;
  border-radius: 50%;
  vertical-align: middle;
  border: 1px solid hsl(237, 14%, 26%);
  -webkit-appearance: none;
  outline: none;
  cursor: pointer;
  margin: 0 0 0 10px;
}

input[type='checkbox']:checked {
  padding: 5px;
  content: url('~@/assets/images/icon-check.svg');
  background: linear-gradient(
    to right,
    hsl(192, 100%, 67%),
    hsl(280, 87%, 65%)
  );
}

input[type='text'] {
  padding: 20px 20px;
  border-style: none;
  background: hsl(235, 24%, 19%);
  outline: none;
  color: white;
}
</style>
