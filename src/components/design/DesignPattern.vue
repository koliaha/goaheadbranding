<template>
  <div class="container">
    <h1 class="text-title">Паттерны</h1>
    <p class="text-prime title__text design-logo-wrapper">
      Паттерны дополняют визуальный контент.
      <br />
      <br />
      Мы создали паттерны из геометрических фигур — из них можно составлять
      разные композиции.
    </p>
    <div class="pattern-section pattern-first">
      <h3 class="text-prime">Контурные</h3>
      <div class="pattern-list">
        <div class="pattern-item pattern-item__left">
          <PatternItem />
        </div>
        <div class="pattern-item">
          <PatternItem />
        </div>
      </div>
    </div>
    <div class="pattern-section pattern-second">
      <div class="pattern-list">
        <div class="pattern-item pattern-item__left">
          <PatternItem />
        </div>
        <div class="pattern-item">
          <PatternItem />
        </div>
      </div>
    </div>
    <div class="pattern-section pattern-third">
      <div class="pattern-list">
        <div class="pattern-item pattern-item__left">
          <PatternItem />
        </div>
        <div class="pattern-item">
          <PatternItem />
        </div>
      </div>
    </div>
    <p class="text-prime title__text design-logo-wrapper pattern-text-bottom mt-120">
      Можно набирать эти знаки на клавиатуре.
    </p>
    <div class="pattern-section pattern-forth">
      <div class="pattern-list">
        <div class="pattern-item">
          <img
            src="@/assets/img/patterns/3.svg"
            alt="patterns"
            class="pattern-item__img"
          />
          <img
            src="@/assets/img/patterns/4.svg"
            alt="patterns"
            class="pattern-item__img"
          />
          <img
            src="@/assets/img/patterns/5.svg"
            alt="patterns"
            class="pattern-item__img"
          />
        </div>
        <div class="pattern-item">
          <img
            src="@/assets/img/patterns/6.svg"
            alt="patterns"
            class="pattern-item__img"
          />
          <img
            src="@/assets/img/patterns/7.svg"
            alt="patterns"
            class="pattern-item__img"
          />
        </div>
      </div>
    </div>
    <div class="pattern-gradient mt-120">
      <img
        class="pattern-gradient__img"
        src="@/assets/img/slides/81.png"
        alt=""
      />
      <img
        class="pattern-gradient__img"
        src="@/assets/img/slides/82.png"
        alt=""
      />
    </div>
    <h3 class="text-prime mb-40 text-center mt-120">
      <b>Примеры использования паттернов</b>
    </h3>
    <TheSwiper :list-image="items" />
    <div class="design-color-link mt-120">
      <a
        href="https://disk.yandex.ru/d/-FV-PZdrBf_ANw"
        target="_blank"
        class="btn text-prime mx-30 btn-wide"
        >Скачать паттерны в PNG</a
      >
      <a
        href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?type=design&node-id=347%3A3060&t=J0bzbmh4GmgJPdZ1-1"
        target="_blank"
        class="btn btn-light text-prime mx-30"
        >Гайд по паттернам</a
      >
    </div>
  </div>
</template>
<script>
import TheSwiper from "@/components/TheSwiper.vue";
import PatternItem from "@/components/design/PatternItem.vue";
export default {
  components: {
    TheSwiper,
    PatternItem,
  },
  data() {
    return {
      items: [
        { content: 31, width: 402 },
        { content: 32, width: 402 },
        { content: 33, width: 717 },
        { content: 34, width: 649 },
        { content: 35, width: 226 },
      ],
    };
  },
};
</script>
<style lang="scss">
  .pattern-text-bottom{
    margin-bottom: 40px;
  }
</style>