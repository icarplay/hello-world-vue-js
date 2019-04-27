<template>
    <div class="tarefas" @click="$emit('alterarStatus', tarefa)" :class="statusTarefa">
        <span class="fechar">X</span>
        <p>{{tarefa.conteudo}}</p>
    </div>
</template>

<script>
export default {
    name: "tarefa",
    props: {
        tarefa: {
            type: Object,
            required: true
        }
    },
    computed: {
        statusTarefa() {
            return {
                pendente: this.tarefa.pendente,
                concluida: !this.tarefa.pendente
            }
        }
    }
}
</script>

<style scoped>
    
    .tarefas {
        position: relative;
        box-sizing: border-box;
        width: 300px;
        height: 125px;
        padding: 10px;
        cursor: pointer;
        user-select: none;
        display: flex;
        justify-content: center;
        align-items: center;
        word-wrap: break-word;
        border-radius: 20px;
        font-size: 25px;
        color: white;
    }

    .fechar {
        position: absolute;
        right: 10px;
        top: 10px;
        font-size: 20px;
        font-weight: 600;
        height: 25px;
        width: 25px;
        border-radius: 25px;
        display: flex;
        justify-content: center;
    }

    .pendente {
        background-color: red
    }

    .concluida {
        background-color: green;
        text-decoration: line-through;
    }

</style>
