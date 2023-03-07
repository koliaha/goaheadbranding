<template>
  <div class="container">
    <h1 class="text-title">Презентация</h1>
    <p class="text-prime  title__text design-logo-wrapper">Презентация — важный инструмент визуального общения с
      клиентами, поэтому все ее компоненты должны легко восприниматься. Основа построения наших слайдов — блочная
      композиционная система.</p>

    <h3 class="text-prime mb-40 text-center"><b>Примеры использования паттернов</b></h3>
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