<template>
  <g>
    <path
      d="M69.945,12.188c-8.138,0-15.368,3.881-19.945,9.892c-4.577-6.011-11.807-9.892-19.945-9.892  C16.217,12.188,5,23.406,5,37.243c0,25.49,45,50.568,45,50.568s45-22.851,45-50.568C95,23.406,83.783,12.188,69.945,12.188z"
    />
  </g>
</template>

<style lang="scss" scoped>
path {
  transform-origin: 50% 50%;
  animation: pop 0.5s cubic-bezier(0.43, 1.37, 0.79, 1.28);
}

@keyframes pop {
  0% {
    opacity: 0;
    transform: scale(0);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
</style>
