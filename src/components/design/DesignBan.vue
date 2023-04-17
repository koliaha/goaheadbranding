<template>
  <div class="container">
    <h1 class="text-title">Баннеры</h1>
    <p class="text-prime  title__text ">Все правила и шаблоны вы найдете в гайде по баннерам
    </p>
    <h3 class="text-prime mb-40 text-center mt-120"><b>Примеры баннеров</b></h3>
  </div>
  <TheSwiper :list-image="[61, 62, 63]" :is-wide="[0,1,2]" :slide-perpage="2"/>
  <div class="container">
    <div class="design-color-link mt-120">
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?t=YF1ac6PQhtuqRvmF-0"
        target="_blank" class="btn text-prime">Гайд по баннерам</a>
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