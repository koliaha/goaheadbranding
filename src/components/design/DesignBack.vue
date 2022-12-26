<template>
  <div class="container">
    <h1 class="text-title">Фоны</h1>
    <p class="text-prime  title__text design-logo-wrapper">Основными цветами фона являются светло- и темно-серые,
      остальные варианты — второстепенные.</p>
    <p class="text-prime  title__text design-logo-wrapper">В некоторых случаях мы используем легкий шум на фоне или
      градиент. Подробнее читайте в гайде по фонам.</p>
    <h3 class="text-prime mb-40 text-center"><b>Примеры использования цвета фона</b></h3>
  </div>
  <TheSwiper :list-image="[1, 2, 3,4]"/>
  <div class="container">
    <p class="text-prime  title__text design-logo-wrapper">Подробнее читайте в гайде по фонам</p>
    <div class="design-color-link">
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=811%3A3185&t=nZNZK5PonXUOwDMj-0"
        target="_blank" class="btn text-prime">Гайд по фонам</a>
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