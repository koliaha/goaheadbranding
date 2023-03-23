<template>
  <div class="container">
    <div class="content-title-wrapper">
      <h1 class="text-title">Презентация</h1>
        <div class="bg-circle circle-content circle-present-fist"></div>
      </div>
    <p class="text-prime  title__text design-present-wrapper">Презентация — важный инструмент визуального общения с
      клиентами, поэтому все ее компоненты должны легко восприниматься. Основа построения наших слайдов — блочная
      композиционная система.</p>

    <h3 class="text-prime mb-40 mt-120 text-center"><b>Примеры использования паттернов</b></h3>
  </div>
  <TheSwiper :list-image="[41, 42, 3]" :is-wide="[0,1,2]" :slide-perpage="2"/>
  <div class="container">
    <p class="text-prime  title__text mt-120 mb-40">Подробнее читайте в гайде по презентации</p>
    <a href="https://disk.yandex.ru/d/FqrDypOnNwqrGw" target="_blank" class="btn text-prime">Гайд по презентации</a>
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