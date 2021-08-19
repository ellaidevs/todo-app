<template>
  <div class="container">
    <div class="input-container">
      <input type="checkbox" />
      <input type="text" placeholder="Create a new todo..." />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
  display: flex;
  border-radius: 5px;
  background: hsl(235, 24%, 19%);
  max-width: 400px;
  /* to arrange the todo title length, check the container max-width above */
  margin: 0 auto;
}

input[type='checkbox'] {
  min-width: 20px;
  min-height: 20px;
  /* padding: 10px; */
  border-radius: 50%;
  vertical-align: middle;
  border: 1px solid hsl(237, 14%, 26%);
  -webkit-appearance: none;
  outline: none;
  cursor: pointer;
  margin: 0 0 0 20px;
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
