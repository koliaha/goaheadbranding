<template>
  <div class="container">
    <h1 class="text-title">Паттерны</h1>
    <p class="text-prime  title__text design-logo-wrapper">Паттерны дополняют визуальный контент.
      <br />
      <br />
      Мы создали паттерны из геометрических фигур — из них можно составлять разные композиции.
    </p>
    <div class="pattern-section pattern-first">
      <h3 class="text-prime">Контурные</h3>
      <div class="pattern-list">
        <div class="pattern-item pattern-item__left">
          <PatternItem/>
        </div>
        <div class="pattern-item">
          <PatternItem/>
        </div>
      </div>
    </div>
    <div class="pattern-section pattern-second">
      <div class="pattern-list">
        <div class="pattern-item pattern-item__left">
          <PatternItem/>
        </div>
        <div class="pattern-item">
          <PatternItem/>
        </div>
      </div>
    </div>
    <div class="pattern-section pattern-third">
      <div class="pattern-list">
        <div class="pattern-item pattern-item__left">
          <PatternItem/>
        </div>
        <div class="pattern-item">
          <PatternItem/>
        </div>
      </div>
    </div>
    <h3 class="text-prime mb-40 text-center"><b>Примеры использования паттернов</b></h3>
  </div>
  <TheSwiper :list-image="[31, 32, 33, 34, 35]" />
  <div class="container">
    <div class="design-color-link mt-120">
      <a href="https://disk.yandex.ru/d/-FV-PZdrBf_ANw" target="_blank" class="btn text-prime mx-30 btn-wide">Скачать
        паттерны в PNG</a>
      <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?t=q6YR4gsn4ay4D8h2-0" target="_blank"
        class="btn btn-light text-prime mx-30">Гайд по паттернам</a>
    </div>
  </div>
</template>
<script>
import TheSwiper from '@/components/TheSwiper.vue'
import PatternItem from '@/components/design/PatternItem.vue'
export default {
  components: {
    TheSwiper,PatternItem
  }
}
</script>