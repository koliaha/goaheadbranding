<template>
  <div class="container">
    <h1 class="text-title">Фоны</h1>
    <p class="text-prime title__text design-back-wrapper">
      Основными цветами фона являются светло- и темно-серые, остальные варианты
      — второстепенные.
    </p>
    <div class="color-back-list">
      <div class="color-row color-back-left">
        <div
          class="color-item__item color-item__item-wide"
          v-for="(i, index) in colorMain"
          :key="index"
        >
          <div
            class="color-item__box"
            :style="{ backgroundColor: `#${i.hex}` }"
          ></div>
          <div class="color-item__title text-prime">{{ i.name }}</div>
          <div class="color-item__descriptions">
            <p>
              <b>RGB</b> <span>{{ roRgb(i.hex) || 0 }}</span>
            </p>
            <p>
              <b>CMYK</b> <span>{{ i.cmyk || 0 }}</span>
            </p>
            <p>
              <b>HEX</b> <span>{{ i.hex || 0 }}</span>
            </p>
          </div>
        </div>
      </div>
      <div class="color-item-list color-back-right">
        <div
          class="color-item__item"
          v-for="(i, index) in colorList"
          :key="index"
        >
          <div
            class="color-item__box color-item__item-border"
            :style="{ backgroundColor: `#${i.hex}` }"
          ></div>
          <div class="color-item__title">{{ i.name }}</div>
          <div class="color-item__descriptions">
            <p>
              <b>RGB</b> <span>{{ roRgb(i.hex) || 0 }}</span>
            </p>
            <p>
              <b>CMYK</b> <span>{{ i.cmyk || 0 }}</span>
            </p>
            <p>
              <b>HEX</b> <span>{{ i.hex || 0 }}</span>
            </p>
          </div>
        </div>
      </div>
      <p class="color-back-text">
        Черный как фон используется только для проставления акцента.
      </p>
    </div>
    <p class="text-prime title__text design-back-wrapper">
      В некоторых случаях мы используем легкий шум на фоне или градиент.
      Подробнее читайте в гайде по фонам.
    </p>
    <h3 class="text-prime mb-40 mt-120 text-center">
      <b>Примеры использования цвета фона</b>
    </h3>
  </div>
  <TheSwiper :list-image="[1, 2, 3, 4]" :is-wide="[2]"/>
  <div class="container">
    <p class="text-prime mb-40 mt-120 title__text design-back-wrapper">
      Подробнее читайте в гайде по фонам
    </p>
    <div class="design-imidge-link">
      <a
        href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=811%3A3185&t=nZNZK5PonXUOwDMj-0"
        target="_blank"
        class="btn text-prime"
        >Гайд по фонам</a
      >
    </div>
  </div>
</template>
<script>
import TheSwiper from "@/components/TheSwiper.vue";
import { color_back, color_back_mini } from "@/datas/colors";
export default {
  components: {
    TheSwiper,
  },
  computed: {
    colorList() {
      return color_back_mini;
    },
    colorMain() {
      return color_back;
    },
  },
  methods: {
    roRgb(str) {
      let aRgbHex = str.match(/.{1,2}/g);
      let aRgb = [
        parseInt(aRgbHex[0], 16),
        parseInt(aRgbHex[1], 16),
        parseInt(aRgbHex[2], 16),
      ];
      return aRgb.join(" ");
    },
  },
};
</script>
<style lang="scss">
@use "@/assets/scss/abstracts" as *;

.design-back-wrapper {
  max-width: 868px;
}

.color-back-list {
  @include flex(row, space-between, start);
  margin-top: 60px;
  margin-bottom: 70px;
}

.color-row {
  @include flex(row);
  gap: 16px;
}

.color-back-left {
  max-width: 510px;
  width: 100%;

  .color-item__item-wide {
    max-width: 247px;
  }

  .color-item__box {
    height: 150px;
  }

  .color-item__title {
    font-size: 24px;
    line-height: 29px;
  }
}

.color-back-right {
  max-width: 188px;
  width: 100%;
}

.color-back-text {
  max-width: 257px;
  width: 100%;
}
</style>
