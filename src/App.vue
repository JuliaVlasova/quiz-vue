<script setup>
import LeftPart from './components/LeftPart.vue'
import Quiz from './components/Quiz.vue'

</script>

<template>
  <header>
    <img alt="logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <LeftPart msg="Викторина!" />
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
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
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
