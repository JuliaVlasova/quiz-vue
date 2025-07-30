<script setup>

</script>

<template>
  <div class="palm">
    <div class="trunk"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="leaf"></div>
    <div class="shadow"></div>
  </div>
</template>

<style>
.palm {
  position: absolute;
  left: 0;
  bottom: 0;
  z-index: 1;
}

/* Ствол пальмы */
.trunk {
  width: 20px;
  height: 70vh;
  background: #8B4513;
  position: relative;
  margin: 0 0 0 40px;
  border-radius: 10px;
}

/* Текстура на стволе */
.trunk::before {
  content: "";
  position: absolute;
  top: 20px;
  left: 5px;
  width: 10px;
  height: 110px;
  background: #A0522D;
  opacity: 0.6;
}

/* Листья пальмы */
.leaf {
  position: absolute;
  width: 0;
  height: 0;
  border-left: 40px solid transparent;
  border-right: 40px solid transparent;
  border-bottom: 180px solid #228B22;
  border-radius: 100%;
}

.leaf:nth-child(2) {
  top: -56px;
  left: -23px;
  transform: rotate(-160deg);
}

.leaf:nth-child(3) {
  top: -54px;
  left: 10px;
  transform: rotate(161deg);
}

.leaf:nth-child(4) {
  top: -77px;
  left: 47px;
  transform: rotate(130deg);
}

.leaf:nth-child(5) {
  top: -52px;
  left: -10px;
  transform: rotate(188deg);
  border-bottom-color: #32CD32;
  border-radius: 100%;
}

.leaf:nth-child(6) {
  top: -70px;
  left: 40px;
  transform: rotate(140deg);
  border-bottom-color: #006400;
}

.leaf:nth-child(7) {
  top: -56px;
  left: 52px;
  transform: rotate(-232deg);
  z-index: -1;
}

.leaf:nth-child(8) {
  top: -37px;
  left: 10px;
  transform: rotate(180deg);
}

.leaf:nth-child(9) {
  top: -62px;
  left: 32px;
  transform: rotate(156deg);
  border-bottom-color: green;
}

.leaf:nth-child(10) {
  top: -82px;
  left: 50px;
  transform: rotate(121deg);
  border-bottom-color: #32CD32;
  border-radius: 100%;
  z-index: -1;
}

.leaf:nth-child(11) {
  top: -69px;
  left: 18px;
  transform: rotate(163deg);
  border-bottom: 173px solid #006400;
  border-left: 26px solid transparent;
}


/* Тень ствола */
.shadow {
  width: 60px;
  height: 20px;
  background: rgba(0, 0, 0, 0.3);
  border-radius: 50%;
  position: absolute;
  bottom: -5px;
  left: 41px;
  transform: rotate(3deg);
  z-index: -1;
}
</style>
