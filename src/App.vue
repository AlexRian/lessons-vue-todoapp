<template>
  <div class="tasks">
    <TasksList v-bind:tasks="tasks"/>
    <TasksForm @save="onTaskChange" />
  </div>
</template>

<script>
import TasksList from '@/components/TasksList.vue'
import TasksForm from '@/components/TasksForm.vue'

export default {
  name: 'App',
  components: {
    TasksList,
    TasksForm
  },
  data () {
    return {
      tasks: [
        {title: "Task One", date: "01.02"},
        {title: "Task Two", date: "02.04"},
      ]
    }
  },
  methods: {
    onTaskChange (data) {
      this.tasks.push(data)
    }
  },
}
</script>

<style lang="scss">
  body{
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .tasks{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    width: 50%;
    &__list{
      // background-color: red;
      width: 100%;
      height: 70vh;
      border: 1px solid black;
    }
    &__form{
      width: 100%;
      height: 30vh;
      // background-color: green;
      border: 1px solid black;

      display: flex;
      align-items: center;
      flex-direction: column;
      padding-top: 10vh;
    }
  }

</style>
