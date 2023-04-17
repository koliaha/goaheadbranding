<template>
  <div class="container">
    <h1 class="text-title">Имиджи</h1>
    <p class="text-prime  title__text ">Мы используем следующие типы имиджей:
    </p>
    <ul class="text-prime">
      <li>3D</li>
      <li>Коллаж</li>
      <li>Фотографии</li>
    </ul>
    <p class="text-prime  title__text design-logo-wrapper">С подробными правилами и примерами вы можете ознакомиться в нашем гайде в фигме
    </p>
    <h3 class="text-prime mb-40 text-center"><b>Примеры имиджей</b></h3>
  </div>
  <TheSwiper :list-image="[71, 72, 73, 74, 75, 76]" />
  <div class="container">
    <p class="text-prime title__text mt-120 mb-40">Подробнее читайте в гайде поимиджам </p>
    <div class="design-imidge-link mt-120">
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?t=LNW5IEoAzuKefvvH-0"
        target="_blank" class="btn text-prime">Гайд по имиджам</a>

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
<style lang="scss">
  .design-imidge-link{
    margin: 20px 0;
    a{
      margin: 15px 0;
    }
  }
</style>