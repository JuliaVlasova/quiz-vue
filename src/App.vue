<script setup>
import LeftPart from './components/LeftPart.vue'
import Quiz from './components/Quiz.vue'

</script>

<template>
  <header>
    <div class="wrapper">
      <LeftPart msg="Какое вы растение?" />
    </div>
  </header>

  <main>
    <Quiz />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    place-items: center;
    flex: 1;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
