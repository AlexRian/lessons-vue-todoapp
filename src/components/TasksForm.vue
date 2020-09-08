<template>
  <div class="tasks__form">
    <input type="text" placeholder="Имя" v-model="taskData.title">
    <input type="text" placeholder="Дата" v-model="taskData.date">
    <button @click="saveTask()">Сохранить</button>
  </div>
</template>

<script>
export default {
  name: 'TaskForm',
  data () {
    return {
      taskData: {
        title: '',
        date: ''
      }
    }
  },
  methods: {
    saveTask () {
      this.$emit('save', this.taskData)
    }
  }
}
</script>

<style scoped lang="scss">
</style>
