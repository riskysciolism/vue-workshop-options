<template>
  <todo-list v-bind:socketResource="'localhost:3000'"></todo-list>
</template>

<script>
import TodoList from './components/todo-list'

export default {
  name: 'App',
  components: {
    TodoList
  }
}
</script>

<style>

</style>
