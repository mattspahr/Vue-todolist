<template>
  <div class="todo-container">
    <div v-bind:key="todo.id" v-for="todo in todos">
      <TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem';
export default {
  name: 'Todos',
  props: ['todos'],
  components: {
    TodoItem
  }
};
</script>

<style scoped>
.todo-container {
  width: 80%;
  margin-left: 10%;
  margin-right: 10%;
  padding-top: 1%;
}
</style>
