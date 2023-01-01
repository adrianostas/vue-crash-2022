<template>
  <div v-for="task in tasks" :key="task.id">
    <Task @toggle-task="$emit('toggle-task', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task"/>

  </div>

</template>

<script>

import Task from './Task-Component.vue'

export default {
  name: "Tasks-Component",
  props: {
    tasks: Array
  },
  components: {
    Task
  },
  emits: ['delete-task', 'toggle-task']
}
</script>

<style scoped>

</style>