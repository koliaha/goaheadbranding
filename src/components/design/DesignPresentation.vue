<template>
  <div class="container">
    <div class="content-title-wrapper">
      <h1 class="text-title">Презентация</h1>
        <div class="bg-circle circle-content circle-present-fist"></div>
      </div>
    <p class="text-prime  title__text design-present-wrapper">Презентация — важный инструмент визуального общения с
      клиентами, поэтому все ее компоненты должны легко восприниматься. Основа построения наших слайдов — блочная
      композиционная система.</p>

    <h3 class="text-prime mb-40 mt-120 text-center"><b>Примеры использования презентаций</b></h3>
  <TheSwiper :list-image="items" :slide-perpage="2"/>
  <p class="text-prime  title__text mt-120 mb-40">Подробнее читайте в гайде по презентации</p>
    <a href="https://disk.yandex.ru/d/FqrDypOnNwqrGw" target="_blank" class="btn text-prime">Гайд по презентации</a>
  </div>
</template>
<script>
import TheSwiper from '@/components/TheSwiper.vue'
export default {
  components: {
    TheSwiper
  },
  data() {
    return {
      items: [
        { content: 41, width: 650 },
        { content: 42, width: 650 },
        { content: 3, width: 650 },
      ],
    };
  },
}
</script>