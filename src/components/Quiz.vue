<script setup>
import QuizItem from './QuizItem.vue'
import QuizLabel from './QuizLabel.vue'
import Palm from './background/Palm.vue'

import { ref } from 'vue';

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
  console.log(sum);
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
    <h3>Ответьте на вопросы - и узнайте всю правду о себе</h3>

    <QuizItem labelsHeader="1. Как вы проводите выходные?" v-if="currentBlockIndex === 0">
      <QuizLabel labelsId="option1" labelsValue="1" labelsName="block-1"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Активно – в походах, на природе.
      </QuizLabel>
      <QuizLabel labelsId="option2" labelsValue="2" labelsName="block-1"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Спокойно – читаю, смотрю фильмы.
      </QuizLabel>
      <QuizLabel labelsId="option3" labelsValue="3" labelsName="block-1"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        В компании друзей.
      </QuizLabel>
      <QuizLabel labelsId="option4" labelsValue="4" labelsName="block-1"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        За творчеством – рисую, пишу, делаю что-то руками.
      </QuizLabel>
      <QuizLabel labelsId="option5" labelsValue="5" labelsName="block-1"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Где-то между уютом и приключениями.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="2. Ваша реакция на стресс?" v-if="currentBlockIndex === 1" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option6" labelsValue="6" labelsName="block-2"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Иду в спортзал или на пробежку.
      </QuizLabel>
      <QuizLabel labelsId="option7" labelsValue="7" labelsName="block-2"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Завариваю чай и жду, пока само пройдет.
      </QuizLabel>
      <QuizLabel labelsId="option8" labelsValue="8" labelsName="block-2"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Звоню друзьям, чтобы выговориться.
      </QuizLabel>
      <QuizLabel labelsId="option9" labelsValue="9" labelsName="block-2"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Выражаю эмоции через творчество.
      </QuizLabel>
      <QuizLabel labelsId="option10" labelsValue="10" labelsName="block-2"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Стараюсь рационально решить проблему.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="3. Какой климат вам ближе?" v-if="currentBlockIndex === 2" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option11" labelsValue="11" labelsName="block-3"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Горы, леса, свежий воздух.
      </QuizLabel>
      <QuizLabel labelsId="option12" labelsValue="12" labelsName="block-3"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Тепло, но не жарко – умеренный.
      </QuizLabel>
      <QuizLabel labelsId="option13" labelsValue="13" labelsName="block-3"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Солнечный и сухой.
      </QuizLabel>
      <QuizLabel labelsId="option14" labelsValue="14" labelsName="block-3"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Переменчивый – люблю разные погоды.
      </QuizLabel>
      <QuizLabel labelsId="option15" labelsValue="15" labelsName="block-3"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Главное, чтобы уютно.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="4. Ваш стиль в одежде?" v-if="currentBlockIndex === 3" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option16" labelsValue="16" labelsName="block-4"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Спортивный, удобный.
      </QuizLabel>
      <QuizLabel labelsId="option17" labelsValue="17" labelsName="block-4"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Классический, минимализм.
      </QuizLabel>
      <QuizLabel labelsId="option18" labelsValue="18" labelsName="block-4"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Яркий, обращающий на себя внимание.
      </QuizLabel>
      <QuizLabel labelsId="option19" labelsValue="19" labelsName="block-4"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Необычный, с элементами handmade.
      </QuizLabel>
      <QuizLabel labelsId="option20" labelsValue="20" labelsName="block-4"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Зависит от настроения.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="5. Как вы ведёте себя в конфликте?" v-if="currentBlockIndex === 4" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option21" labelsValue="21" labelsName="block-5"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Твердо стою на своём.
      </QuizLabel>
      <QuizLabel labelsId="option22" labelsValue="22" labelsName="block-5"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Стараюсь избегать ссор.
      </QuizLabel>
      <QuizLabel labelsId="option23" labelsValue="23" labelsName="block-5"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Эмоционально включаюсь, но быстро отхожу.
      </QuizLabel>
      <QuizLabel labelsId="option24" labelsValue="24" labelsName="block-5"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Ищу нестандартный выход.
      </QuizLabel>
      <QuizLabel labelsId="option25" labelsValue="25" labelsName="block-5"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Анализирую и пытаюсь договориться.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="6. Что важнее в жизни?" v-if="currentBlockIndex === 5" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option26" labelsValue="26" labelsName="block-6"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Свобода и приключения.
      </QuizLabel>
      <QuizLabel labelsId="option27" labelsValue="27" labelsName="block-6"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Гармония и стабильность.
      </QuizLabel>
      <QuizLabel labelsId="option28" labelsValue="28" labelsName="block-6"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Яркие эмоции и впечатления.
      </QuizLabel>
      <QuizLabel labelsId="option29" labelsValue="29" labelsName="block-6"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Самореализация и творчество.
      </QuizLabel>
      <QuizLabel labelsId="option30" labelsValue="30" labelsName="block-6"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Баланс между разным.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="7. Ваше отношение к одиночеству?" v-if="currentBlockIndex === 6" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option31" labelsValue="31" labelsName="block-7"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Мне комфортно одному, но и в компании хорошо.
      </QuizLabel>
      <QuizLabel labelsId="option32" labelsValue="32" labelsName="block-7"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Люблю уединение.
      </QuizLabel>
      <QuizLabel labelsId="option33" labelsValue="33" labelsName="block-7"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Не люблю быть один/одна.
      </QuizLabel>
      <QuizLabel labelsId="option34" labelsValue="34" labelsName="block-7"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Одиночество – время для вдохновения.
      </QuizLabel>
      <QuizLabel labelsId="option35" labelsValue="35" labelsName="block-7"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Всё зависит от ситуации.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="8. Какой вы в работе?" v-if="currentBlockIndex === 7" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option36" labelsValue="36" labelsName="block-8"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Энергичный, быстро принимаю решения.
      </QuizLabel>
      <QuizLabel labelsId="option37" labelsValue="37" labelsName="block-8"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Усидчивый, внимательный к деталям.
      </QuizLabel>
      <QuizLabel labelsId="option38" labelsValue="38" labelsName="block-8"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Коммуникабельный, люблю командную работу.
      </QuizLabel>
      <QuizLabel labelsId="option39" labelsValue="39" labelsName="block-8"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Креативный, нестандартный.
      </QuizLabel>
      <QuizLabel labelsId="option40" labelsValue="40" labelsName="block-8"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Адаптируюсь под задачу.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="9. Какие книги/фильмы вам нравятся?" v-if="currentBlockIndex === 8" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option41" labelsValue="41" labelsName="block-9"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Приключения, фэнтези.
      </QuizLabel>
      <QuizLabel labelsId="option42" labelsValue="42" labelsName="block-9"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Классика, философские произведения.
      </QuizLabel>
      <QuizLabel labelsId="option43" labelsValue="43" labelsName="block-9"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Драмы, романтические истории.
      </QuizLabel>
      <QuizLabel labelsId="option44" labelsValue="44" labelsName="block-9"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Арт-хаус, необычные сюжеты.
      </QuizLabel>
      <QuizLabel labelsId="option45" labelsValue="45" labelsName="block-9"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Разные жанры, но с глубиной.
      </QuizLabel>
    </QuizItem>
    <QuizItem labelsHeader="10. Какой вы в любви?" v-if="currentBlockIndex === 9" @clickUpdate="(event) => {
      console.log('Quiz.vue received click:', event);
      goToNextBlock(event);
    }">
      <QuizLabel labelsId="option46" labelsValue="46" labelsName="block-10"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Страстный и независимый.
      </QuizLabel>
      <QuizLabel labelsId="option47" labelsValue="47" labelsName="block-10"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Верный и спокойный.
      </QuizLabel>
      <QuizLabel labelsId="option48" labelsValue="48" labelsName="block-10"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Эмоциональный и романтичный.
      </QuizLabel>
      <QuizLabel labelsId="option49" labelsValue="49" labelsName="block-10"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Непредсказуемый и творческий.
      </QuizLabel>
      <QuizLabel labelsId="option50" labelsValue="50" labelsName="block-10"
        @clickUpdate="(event) => { goToNextBlock(event); }">
        Гибкий и понимающий.
      </QuizLabel>
    </QuizItem>
  </div>

  <div v-if="currentBlockIndex >= 10">
    Ваш результат: {{ resultText }}
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
</style>


<!-- Общий фон - пальма, макака, свисающая сверху. Куча всякой анимации. Пляжный сезон. -->