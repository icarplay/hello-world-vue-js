<template>
  <div id="app">
    <h1>Lista de Tarefas</h1>
    <listaTarefas :tarefas=tarefas></listaTarefas>
  </div>
</template>

<script>

import listaTarefas from './components/listaTarefas'

export default {
  name: 'app',
  components: {
    listaTarefas
  },
  data() {
    return {
      tarefas:  [
                  {conteudo: "Terminar o curso", status: true},
                  {conteudo: "Terminar o dia", status: false}
                ]
    }
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
