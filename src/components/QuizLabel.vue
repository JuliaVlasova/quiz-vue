<script setup>
const props = defineProps({
    labelsValue: {
        type: String,
        required: true,
        default: "Вы забыли указать значение!!!"
    },
    labelsId: {
        type: String,
        required: true,
        default: "Вы забыли указать id!!!"
    },
    labelsName: {
        type: String,
        required: true,
        default: "Name одинаковый для одного блока"
    }
})
</script>

<template>
    <label :for="labelsId" class="quiz-label">
        <input type="radio" :name="labelsName" :id="labelsId" :value="labelsValue">
        <span><slot></slot></span>
    </label>
</template>

<style scoped>
.labels-block {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.quiz-label {
    display: flex;
    gap: 10px;
}

.quiz-label input {
    --size: 20px;
    width: var(--size);
    height: var(--size);
    margin-top: 2px;
}
</style>
