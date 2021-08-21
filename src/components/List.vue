<template>
  <div class="container">
    <div class="header-input">
      <div class="input-container">
        <input type="checkbox" v-model="checkbox" />
        <input
          type="text"
          placeholder="Create a new todo..."
          v-model="todo"
          @keyup.enter="addTodo"
        />
      </div>
    </div>
    <div class="list" v-for="todo in todoList" :key="todoList.indexOf(todo)">
      <div>
        <input class="list-checkbox" type="checkbox" :checked="todo.active" />
        <input type="text" :value="todo.todo" disabled />
      </div>
    </div>
    <div class="counter">
      <div class="list">
        <div class="clear" v-if="todoList.length > 1">
          {{ todoList.length }} items left
        </div>
        <div class="clear" v-else>{{ todoList.length }} item left</div>
        <div class="clear-completed clear">Clear completed</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      todoList: [],
      todo: '',
      checkbox: false,
    }
  },
  methods: {
    addTodo() {
      const todoObj = {
        todo: this.todo,
        active: this.checkbox,
      }
      this.todoList.push(todoObj)
      this.todo = ''
      console.log(this.todoList)
    },
  },
}
</script>

<style scoped>
.header-input,
.list {
  display: flex;
  border-radius: 7px;
  background: hsl(235, 24%, 19%);
  max-width: 400px;
  margin: 0 auto 20px auto;
}

input[type='text'] {
  font-family: 'Josefin Sans', sans-serif;
  font-size: 18px;
  padding: 20px 20px;
  border-style: none;
  background: hsl(235, 24%, 19%);
  outline: none;
  color: hsl(234, 39%, 85%);
}

input[type='text']:hover {
  color: hsl(236, 33%, 92%);
}

input[type='checkbox'] {
  min-width: 20px;
  min-height: 20px;
  border-radius: 50%;
  vertical-align: middle;
  border: 1px solid hsl(237, 14%, 26%);
  -webkit-appearance: none;
  outline: none;
  cursor: pointer;
  margin: 0 0 0 20px;
  /* create a mobile view and reduce the left margin, */
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

.list {
  margin: 0 auto;
  border-radius: 0px;
  border-bottom: 1px solid hsl(233, 14%, 35%);
}

div.list:nth-child(2) {
  border-radius: 7px 7px 0 0;

  /* todo: add fix border-radius when only one list exist */
}

.list:nth-last-child(2) {
  border-radius: 0 0 7px 7px;
  border-bottom: none;
}

.counter {
  margin: 25px auto;
}

.counter > .list {
  display: flex;
  color: hsl(234, 39%, 85%);
  font-size: 14px;
  min-height: 60px;
  border-radius: 7px;
}

.clear {
  margin: auto;
}

.clear-completed {
  cursor: pointer;
}

.clear-completed:hover {
  color: hsl(236, 33%, 92%);
}
</style>
