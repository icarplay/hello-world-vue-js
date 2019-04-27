<template>
    <div class="lista">
        <tarefa class="tarefa" 
                v-for="(tarefa, index) in tarefas"
                :tarefa="tarefa"
                :key="tarefa.conteudo"
                @alterarStatus="$emit('alterarStatus', index)"
        ></tarefa>
    </div>
</template>


<script>

import tarefa from './tarefa'

export default {
    nome: "listaTarefas",
    components: {
        tarefa
    },
    props: {
        tarefas: {
            type: Array,
            required: true
        }
    }
}
</script>


<style scoped>
    .lista {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }

    .lista .tarefa {
        margin: 10px
    }
</style>
