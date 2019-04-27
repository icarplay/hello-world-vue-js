<template>
    <div>
        <p v-for="tarefa in tarefas" :key="tarefa">
            {{ tarefa.conteudo }}
        </p>
    </div>
</template>


<script>
export default {
    nome: "listaTarefas",
    props: {
        tarefas: {
            type: Array,
            required: true
        }
    }
}
</script>


<style scoped>
</style>
