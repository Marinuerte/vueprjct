<script>
import TaskApp from './components/TaskApp.vue';
export default {
  components: {
    TaskApp,
  }
}
</script>
<template>
  <div class="container mt-5">
    <TaskApp />
  </div>
</template>
<style>
.container {
  max-width: 600px;
  margin: 0 auto;
}
</style>