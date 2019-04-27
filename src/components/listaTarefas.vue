<template>
    <h1>Teste</h1>
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
