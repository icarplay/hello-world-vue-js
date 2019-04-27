<template>
    <div class="tarefas">
        <span class="fechar">X</span>
        <p></p>
    </div>
</template>

<script>
export default {
    name: "tarefa"
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

</style>
