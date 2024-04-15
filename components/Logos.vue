<template>
  <svg id="logos" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <path
      class="stroke-primary"
      stroke-width="2" fill="none"
      stroke-linecap="square"
      d="
        M3 6 C8 0 16 12 21 6
        M3 12 C8 4 16 16 21 12
        M3 18 C8 8 16 22 21 18
      "
    />
  </svg>
</template>

<style scoped>
  #logos path {
  stroke-dashoffset: 1px;
  stroke-dasharray: 0 30px;
  animation: grow 5s ease forwards infinite;
  transform-origin: center;
}

@keyframes grow {
  0% {
    stroke-dashoffset: 1px;
    stroke-dasharray: 0 30px;
    opacity: 0;
  }
  10% {
    opacity: 1;
  }
  40% {
    stroke-dasharray: 30px 0;
  }
  /* Moving back */
  99% {
    stroke-dasharray: 30px 0;
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
</style>
