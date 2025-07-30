<script setup>
import { defineEmits } from 'vue';

const props = defineProps({
    labelsHeader: {
        type: String,
        required: true,
        default: "Вы забыли указать заголовок!!!"
    }
})

const emit = defineEmits(['clickUpdate']);

</script>

<template>
    <h2 class="labels-header">{{ labelsHeader }}</h2>
    <div class="labels-block">
        <slot></slot>
    </div>
</template>

<style scoped>
.labels-block {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.labels-header {
    margin-top: 20px;
    margin-bottom: 10px;
}
</style>
