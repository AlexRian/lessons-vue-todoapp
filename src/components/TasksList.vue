<template>
  <div class="tasks__list">
    <h3 v-for="task in tasks" :key="task.id">{{task.title}} - {{task.date}}</h3>
  </div>
</template>

<script>
export default {
  name: 'TasksList',
  props: [
    'tasks'
  ],
}
</script>

<style scoped lang="scss">

</style>
