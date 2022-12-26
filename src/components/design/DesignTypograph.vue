<template>
    <div class="container">
      <h1 class="text-title">Типографика</h1>
      <p class="text-prime  title__text design-logo-wrapper">В брендированных креативах мы сочетаем акцентный шрифт с наборным, чтобы текст привлекал внимание.</p>
      
      <h3 class="text-prime mb-40 text-center"><b>Примеры применения типографики</b></h3>
    </div>
    <TheSwiper :list-image="[11, 12, 13,14]"/>
    <div class="container">
      <div class="design-color-link">
        <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=347%3A1243&t=lXHVzUJeuQw3y50q-0"
          target="_blank" class="btn text-prime">Гайд по типографике</a>
      </div>
    </div>
  </template>
  <script>
  import TheSwiper from '@/components/TheSwiper.vue'
  export default {
    components: {
      TheSwiper
    }
  }
  </script>