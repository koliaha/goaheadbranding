<template>
  <div class="container">
    <div class="content-title-wrapper">
      <h1 class="text-title">SMM</h1>
        <div class="bg-circle circle-content circle-smm-fist"></div>
      </div>
    
    <p class="text-prime  title__text design-smm-wrapper">Социальные сети — инструмент менее формального общения с аудиторией, поэтому здесь приветствуется бОльшая креативность и смелость.
    </p>
    <p class="text-prime  title__text design-smm-wrapper">Для оформления постов в инстаграм и другие соцсети можно использовать следующие техники:
    </p>
    <ul class="text-prime">
      <li>3D</li>
      <li>Коллажи</li>
      <li>Шрифтовая композиция + паттерн</li>
      <li>Наши собственные фотографии без текста (например, с мероприятий)</li>
    </ul>

    <h3 class="text-prime mb-40 text-center mt-120"><b>Примеры SMM</b></h3>
  </div>
  <TheSwiper :list-image="[51, 52, 53,54,55]"/>
  <div class="container">
    <p class="text-prime  title__text mt-120 mb-40">Подробнее читайте в гайде по SMM </p>
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?t=mttvpFdAd2o2WFPi-0"
        target="_blank" class="btn text-prime ">Гайд по SMM</a>
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
<style lang="scss">
  .design-smm-wrapper{
    max-width:737px;
  }
</style>