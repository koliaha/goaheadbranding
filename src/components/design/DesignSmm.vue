<template>
  <div class="container">
    <h1 class="text-title">SMM</h1>
    <p class="text-prime  title__text design-logo-wrapper">Социальные сети — инструмент менее формального общения с аудиторией, поэтому здесь приветствуется бОльшая креативность и смелость.
    </p>

    
    <h3 class="text-prime mb-40 text-center"><b>Примеры SMM</b></h3>
  </div>
  <TheSwiper :list-image="[51, 52, 53,54,55]"/>
  <div class="container">
    <p class="text-prime  title__text design-logo-wrapper">Подробнее читайте в гайде по SMM
    </p>
    <div class="design-color-link">
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=636%3A2184&t=lXHVzUJeuQw3y50q-0"
        target="_blank" class="btn text-prime">Гайд по SMM</a>
       
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