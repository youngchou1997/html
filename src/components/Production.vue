<template>
  <div class="heart"></div>
</template>

<script>
export default {}
</script>

<style scoped>
.heart {
  width: 198px;
  height: 198px;
  background: #f00;
  position: relative;
  -webkit-animation: heartbeat 1s infinite linear;
  animation: heartbeat 1s infinite linear;
  left: 200px;
  filter: drop-shadow(0px 0px 20px rgb(255, 20, 20));
  top: 100px;
}
.heart::before,
.heart::after {
  background: #f00;
  content: '';
  width: 200px;
  height: 200px;
  border-radius: 100px;
  position: absolute;
}
.heart::before {
  left: -100px;
}
.heart::after {
  left: 0;
  top: -100px;
}
@keyframes heartbeat {
  0% {
    transform: rotate(45deg) scale(1, 1);
    opacity: 0.8;
  }
  25% {
    transform: rotate(45deg) scale(0.8, 0.8);
  }
  100% {
    transform: rotate(45deg) scale(1, 1);
    opacity: 0.8;
  }
}
</style>
