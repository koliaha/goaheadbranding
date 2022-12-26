<template>
  <div class="container">
    <h1 class="text-title">Паттерны</h1>
    <p class="text-prime  title__text design-logo-wrapper">Паттерны дополняют визуальный контент.
<br/>
<br/>
Мы создали паттерны из геометрических фигур — из них можно составлять разные композиции.</p>
    
    <h3 class="text-prime mb-40 text-center"><b>Примеры использования паттернов</b></h3>
  </div>
  <TheSwiper :list-image="[31, 32, 33,34,35]"/>
  <div class="container">
    
    <div class="design-color-link">
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=811%3A3185&t=nZNZK5PonXUOwDMj-0"
        target="_blank" class="btn text-prime">Гайд по фонам</a>
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