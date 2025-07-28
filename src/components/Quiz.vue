<script setup>
import QuizItem from './QuizItem.vue'
import QuizLabel from './QuizLabel.vue'


</script>

<template>
  <div class="">
    <h3>Ответьте на вопросы - и узнайте всю правду о себе</h3>

    <QuizItem labelsHeader="Вы сова или жаворонок?">
      <QuizLabel labelsId="option1" labelsValue="111" labelsName="block-first">
        Первый вопрос первого блока
      </QuizLabel>
      <QuizLabel labelsId="option2" labelsValue="222" labelsName="block-first">
        Второй вопрос первого блока
      </QuizLabel>
    </QuizItem>
    <QuizItem>
      <QuizLabel labelsId="option3" labelsValue="333" labelsName="block-second">
        Первый вопрос второго блока
      </QuizLabel>
      <QuizLabel labelsId="option4" labelsValue="444" labelsName="block-second">
        Второй вопрос второго блока
      </QuizLabel>
    </QuizItem>
  </div>
</template>

<style scoped>
  label {
    cursor: pointer;
  }
</style>
