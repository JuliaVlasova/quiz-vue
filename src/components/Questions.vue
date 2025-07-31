<script>
export function Questions() {
  const questions = {
    question1: {
      header: '1. Как вы проводите выходные?',
      options: [
        { id: 'option1', value: '1', name: 'block-1', text: 'Активно – в походах, на природе.' },
        { id: 'option2', value: '2', name: 'block-1', text: 'Спокойно – читаю, смотрю фильмы.' },
        { id: 'option3', value: '3', name: 'block-1', text: 'В компании друзей.' },
        { id: 'option4', value: '4', name: 'block-1', text: 'За творчеством – рисую, пишу, делаю что-то руками.' },
        { id: 'option5', value: '5', name: 'block-1', text: 'Где-то между уютом и приключениями.' },
      ],
    },
    question2: {
      header: '2. Ваша реакция на стресс?',
      options: [
        { id: 'option6', value: '6', name: 'block-2', text: 'Иду в спортзал или на пробежку.' },
        { id: 'option7', value: '7', name: 'block-2', text: 'Завариваю чай и жду, пока само пройдет.' },
        { id: 'option8', value: '8', name: 'block-2', text: 'Звоню друзьям, чтобы выговориться.' },
        { id: 'option9', value: '9', name: 'block-2', text: 'Выражаю эмоции через творчество.' },
        { id: 'option10', value: '10', name: 'block-2', text: 'Стараюсь рационально решить проблему.' },
      ],
    },
    question3: {
      header: '3. Какой климат вам ближе?',
      options: [
        { id: 'option11', value: '11', name: 'block-3', text: 'Горы, леса, свежий воздух.' },
        { id: 'option12', value: '12', name: 'block-3', text: 'Тепло, но не жарко – умеренный.' },
        { id: 'option13', value: '13', name: 'block-3', text: 'Солнечный и сухой.' },
        { id: 'option14', value: '14', name: 'block-3', text: 'Переменчивый – люблю разные погоды.' },
        { id: 'option15', value: '15', name: 'block-3', text: 'Главное, чтобы уютно.' },
      ],
    },
    question4: {
      header: '4. Ваш стиль в одежде?',
      options: [
        { id: 'option16', value: '16', name: 'block-4', text: 'Спортивный, удобный.' },
        { id: 'option17', value: '17', name: 'block-4', text: 'Классический, минимализм.' },
        { id: 'option18', value: '18', name: 'block-4', text: 'Яркий, обращающий на себя внимание.' },
        { id: 'option19', value: '19', name: 'block-4', text: 'Необычный, с элементами handmade.' },
        { id: 'option20', value: '20', name: 'block-4', text: 'Зависит от настроения.' },
      ],
    },
    question5: {
      header: '5. Как вы ведёте себя в конфликте?',
      options: [
        { id: 'option21', value: '21', name: 'block-5', text: 'Твердо стою на своём.' },
        { id: 'option22', value: '22', name: 'block-5', text: 'Стараюсь избегать ссор.' },
        { id: 'option23', value: '23', name: 'block-5', text: 'Эмоционально включаюсь, но быстро отхожу.' },
        { id: 'option24', value: '24', name: 'block-5', text: 'Ищу нестандартный выход.' },
        { id: 'option25', value: '25', name: 'block-5', text: 'Анализирую и пытаюсь договориться.' },
      ],
    },
    question6: {
      header: '6. Что важнее в жизни?',
      options: [
        { id: 'option26', value: '26', name: 'block-6', text: 'Свобода и приключения.' },
        { id: 'option27', value: '27', name: 'block-6', text: 'Гармония и стабильность.' },
        { id: 'option28', value: '28', name: 'block-6', text: 'Яркие эмоции и впечатления.' },
        { id: 'option29', value: '29', name: 'block-6', text: 'Самореализация и творчество.' },
        { id: 'option30', value: '30', name: 'block-6', text: 'Баланс между разным.' },
      ],
    },
    question7: {
      header: '7. Ваше отношение к одиночеству?',
      options: [
        { id: 'option31', value: '31', name: 'block-7', text: 'Мне комфортно одному, но и в компании хорошо.' },
        { id: 'option32', value: '32', name: 'block-7', text: 'Люблю уединение.' },
        { id: 'option33', value: '33', name: 'block-7', text: 'Не люблю быть один/одна.' },
        { id: 'option34', value: '34', name: 'block-7', text: 'Одиночество – время для вдохновения.' },
        { id: 'option35', value: '35', name: 'block-7', text: 'Всё зависит от ситуации.' },
      ],
    },
    question8: {
      header: '8. Какой вы в работе?',
      options: [
        { id: 'option36', value: '36', name: 'block-8', text: 'Энергичный, быстро принимаю решения.' },
        { id: 'option37', value: '37', name: 'block-8', text: 'Усидчивый, внимательный к деталям.' },
        { id: 'option38', value: '38', name: 'block-8', text: 'Коммуникабельный, люблю командную работу.' },
        { id: 'option39', value: '39', name: 'block-8', text: 'Креативный, нестандартный.' },
        { id: 'option40', value: '40', name: 'block-8', text: 'Адаптируюсь под задачу.' },
      ],
    },
    question9: {
      header: '9. Какие книги/фильмы вам нравятся?',
      options: [
        { id: 'option41', value: '41', name: 'block-9', text: 'Приключения, фэнтези.' },
        { id: 'option42', value: '42', name: 'block-9', text: 'Классика, философские произведения.' },
        { id: 'option43', value: '43', name: 'block-9', text: 'Драмы, романтические истории.' },
        { id: 'option44', value: '44', name: 'block-9', text: 'Арт-хаус, необычные сюжеты.' },
        { id: 'option45', value: '45', name: 'block-9', text: 'Разные жанры, но с глубиной.' },
      ],
    },
    question10: {
      header: '10. Какой вы в любви?',
      options: [
        { id: 'option46', value: '46', name: 'block-10', text: 'Страстный и независимый.' },
        { id: 'option47', value: '47', name: 'block-10', text: 'Верный и спокойный.' },
        { id: 'option48', value: '48', name: 'block-10', text: 'Эмоциональный и романтичный.' },
        { id: 'option49', value: '49', name: 'block-10', text: 'Непредсказуемый и творческий.' },
        { id: 'option50', value: '50', name: 'block-10', text: 'Гибкий и понимающий.' },
      ],
    },
  };
  return questions;
}
</script>



