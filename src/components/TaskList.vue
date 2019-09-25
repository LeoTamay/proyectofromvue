<template>

    <table class="table">
  <thead> 
    <tr>
      <th scope="col">id</th>
      <th scope="col">name</th>
      <th scope="col">description</th>
      <th scope="col">priority</th>
      <th scope="col">status</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="list in tasks.tasks" :key="list.id">
      <th scope="row">{{list.id}}</th>
      <td>{{list.name}}</td>
      <td>{{list.description}}</td>
      <td>{{list.priority}}</td>
      <td>{{list.status}}</td>
    </tr>
  </tbody>
</table>
</template>
<script>

export default {
  name: 'TaskList',
  data(){
    return{
      tasks:[],
    }
  },

  mounted(){
    this.getTask()
  },

  methods: {
      getTask: async function () {
        try {
            const data = await fetch('http://127.0.0.1:8000/api/tasks/')
            this.tasks = await data.json()
            console.log(this.tasks)
        } catch (error) {
                        console.error(error)
                        }
      }
  }
}
</script>