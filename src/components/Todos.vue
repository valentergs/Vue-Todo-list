<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <TodoItem v-bind:todo="todo" v-on:apagar-item="$emit('apagar-item', todo.id)"/>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem.vue";
export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ["todos"]
};
</script>

<style scoped>
</style>


