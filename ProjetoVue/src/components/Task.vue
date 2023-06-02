<template>
    <h1>{{ msg }}</h1>
    <h2 v-for="item in todo">{{ item }}</h2>
    <input type="text" v-model="taskName"/>
    <button v-on:click="add()">Add</button>
  </template>
  
  <script>
  export default (await import('vue')).defineComponent({
    name: 'Task',
    data() {
      return {
        taskName: '',
        msg: 'Componente Task',
        todo: ['Learn Vue', 'Learn Vue Router', 'Lear Vue components']
      }
    },
    methods: {
        add(){
            this.todo.push(this.taskName)
        }
    }
  })
  
  </script>
  
  <style>
  h2{
    text-align: center;
    color: blueviolet;
  }
  h1{
    text-align: center;
    color: darkmagenta;
  }
  input{
    margin-left: 600px;
  }

</style>
  