<template>
  <div>
    <Tasklist></Tasklist>
    <NewTask></NewTask>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Tasklist from './components/TaskList.vue'
import NewTask from './components/NewTask.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Tasklist,
    NewTask
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
