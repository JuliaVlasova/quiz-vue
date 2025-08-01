<script setup>
import { Questions } from './Questions.vue'
import QuizItem from './QuizItem.vue'
import QuizLabel from './QuizLabel.vue'
import Palm from './background/Palm.vue'


import { ref } from 'vue';

const questionsData = Questions();
const currentBlockIndex = ref(0);
const answers = ref([]);
const resultText = ref('');

function goToNextBlock(event) {
  answers.value.push(event);
  currentBlockIndex.value++;

  if (currentBlockIndex.value >= 10) {
    handleResult(answers);
  }
}

function handleResult(data) {
  const numericValues = data.value.map(Number);
  const sum = numericValues.reduce((accumulator, currentValue) => accumulator + currentValue, 0);

  if (sum > 270) {
    resultText.value = `Вы фикус (адаптивный, универсальный, жизнестойкий).`;
  } else if (sum > 260 && sum <= 270) {
    resultText.value = `Вы орхидея (утончённый, творческий, необычный).`;
  } else if (sum > 250 && sum <= 260) {
    resultText.value = `Вы подсолнух (яркий, открытый, тянетесь к людям).`;
  } else if (sum > 240 && sum <= 250) {
    resultText.value = `Вы лавр (мудрый, гармоничный, благородный).`;
  } else if (sum > 230 && sum <= 240) {
    resultText.value = `Вы бамбук (сильный, гибкий, стремитесь вверх).`;
  } else {
    resultText.value = `Вы вид краснокнижный, очень редкий.`;
  }
}
</script>

<template>
  <Palm />
  <div class="right-part">
    <h3 v-if="currentBlockIndex < 10">Ответьте на вопросы - и узнайте всю правду о себе</h3>

    <template v-for="(question, index) in Object.values(questionsData)">
      <QuizItem :key="index" :labelsHeader="question.header"
        v-if="currentBlockIndex === index">
        <QuizLabel v-for="option in question.options" :key="option.id" :labelsId="option.id" :labelsValue="option.value"
          :labelsName="option.name" @clickUpdate="(event) => { goToNextBlock(event); }">
          {{ option.text }}
        </QuizLabel>
      </QuizItem>
    </template>
  </div>

  <div v-if="currentBlockIndex >= 10" class="result-block">
    {{ resultText }}
  </div>
</template>

<style scoped>
label {
  cursor: pointer;
}

.right-part {
  max-height: 95vh;
  overflow: hidden;
  overflow-y: auto;
  padding: 20px;
}

.result-block {
  padding: 40px;
  font-size: 2rem;
  max-width: 300px;
  font-weight: 700;
  color: green;
}
</style>


<!-- Общий фон - пальма, макака, свисающая сверху. Куча всякой анимации. Пляжный сезон. -->