<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 3.6rem;
  position: relative;
  top: -10px;
  color: #008080;
  line-height: 1;
  max-width: 280px;
}


</style>
