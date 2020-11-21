<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Bem vindo"/>
    <div v-for="tarefa in tarefas" :key="tarefa.id">
      <div v-if="tarefa.estacompleta"
        class="completa"
      >
        <h1>Tarefa numero {{tarefa.id}}</h1>
        <p>{{ tarefa.descricao }}</p>
      </div>

      <div v-else
        class="incompleta"
      >
        <h1>Tarefa numero {{tarefa.id}}</h1>
        <p>{{ tarefa.descricao }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      tarefas: [
        {id: 1, descricao: "Tarefa 1", estacompleta: false},
        {id: 2, descricao: "Tarefa 2", estacompleta: true},
        {id: 3, descricao: "Tarefa 3", estacompleta: true},
        {id: 4, descricao: "Tarefa 4", estacompleta: false},
        {id: 5, descricao: "Tarefa 5", estacompleta: true},
        {id: 6, descricao: "Tarefa 6", estacompleta: false},
        {id: 7, descricao: "Tarefa 7", estacompleta: false}
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.completa {
  background-color: green;
}

.incompleta {
  background-color: red;
}
</style>
