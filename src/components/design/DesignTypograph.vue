<template>
  <div class="container">
    <h1 class="text-title">Типографика</h1>
    <p class="text-prime title__text design-logo-wrapper">
      В брендированных креативах мы сочетаем акцентный шрифт с наборным, чтобы
      текст привлекал внимание.
    </p>
    <h3 class="text-prime mb-40 text-center">
      <b>Примеры применения типографики</b>
    </h3>
  </div>
  <TheSwiper :list-image="items" />
  <div class="container">
    <div class="font-wrapper">
      <h2 class="text-center mt-120 mb-40 robo text-title">Robtronika</h2>
      <p class="text-prime title__text mb-40">Акцентный шрифт</p>
      <div class="alphabet-wrapper">
        <div class="alpha-item">
          <div class="alpha-list robo">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-wide"
              v-for="(i, index) in eng_alpha"
              :key="index"
              >{{ i }}</span
            >
          </div>
          <div class="alpha-list mt-40 robo">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-wide"
              v-for="(i, index) in num_list"
              :key="index"
              >{{ i }}</span
            >
          </div>
        </div>
        <div class="alpha-item alpha-item__dark">
          <div class="alpha-list robo">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-wide"
              v-for="(i, index) in ru_alpha"
              :key="index"
              >{{ i }}</span
            >
          </div>
        </div>
      </div>
      <div class="alphabet-wrapper mb-40">
        <div class="alpha-item">
          <div class="alpha-list alpha-list-slim robo">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-slim"
              v-for="(i, index) in sym_list"
              :key="index"
              >{{ i }}</span
            >
          </div>
        </div>
      </div>
      <div class="alphabet-wrapper mb-40">
        <div class="alpha-item">
          <p class="text-prime title__text mb-40 text-center">
            Эти символы не используем
          </p>
          <div class="alpha-list alpha-list-slim">
            <div
              class="alpha-letter alpha-letter-up alpha-letter-slim"
              v-for="(i, index) in nosym_list"
              :key="index"
            >
              <span class="robo">{{ i }}</span>
              <span class="alpha-symbol">{{ i }}</span>
            </div>
          </div>
        </div>
      </div>
      <h2 class="text-center mt-120 mb-40 text-title">Montserrat</h2>
      <p class="text-prime title__text mb-40">Наборный шрифт</p>
      <div class="alphabet-wrapper">
        <div class="alpha-item">
          <div class="alpha-list alpha-list-small">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-wide"
              v-for="(i, index) in eng_alpha"
              :key="index"
              >{{ i }}</span
            >
          </div>
          <div class="alpha-list mt-40">
            <span
              class="alpha-letter alpha-letter-wide"
              v-for="(i, index) in eng_alpha"
              :key="index"
              >{{ i }}</span
            >
          </div>
          <div class="alpha-list mt-40 alpha-list-small">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-wide"
              v-for="(i, index) in sym_list_wide"
              :key="index"
              >{{ i }}</span
            >
          </div>
        </div>
        <div class="alpha-item alpha-item__dark">
          <div class="alpha-list alpha-list-small">
            <span
              class="alpha-letter alpha-letter-up alpha-letter-wide"
              v-for="(i, index) in ru_alpha"
              :key="index"
              >{{ i }}</span
            >
          </div>
          <div class="alpha-list mt-40 alpha-list-small">
            <span
              class="alpha-letter alpha-letter-wide"
              v-for="(i, index) in ru_alpha"
              :key="index"
              >{{ i }}</span
            >
          </div>
          <div class="alpha-list mt-40 alpha-list-slim">
            <span
              class="alpha-letter alpha-letter-wide"
              v-for="(i, index) in num_list"
              :key="index"
              >{{ i }}</span
            >
          </div>
        </div>
      </div>
    </div>
    <div class="design-color-link mt-120">
      <a
        href="https://disk.yandex.ru/d/Hx8lfG5jaFtHzw"
        target="_blank"
        class="btn text-prime"
        >Скачать шрифты</a
      >
    </div>
    <h3 class="text-prime mb-40 mt-120"><b>Наши правила типографики</b></h3>
    <div class="typo-rules">
      <div class="typo-rule-item typo-rule-first">
        <div class="design-logo-rule typo-rule">
          <span class="rule-num">1</span>
          <p class="rule-text text-second">
            Акцентный шрифт используем с градиентным, контурным или монохромным
            оформлением.
          </p>
        </div>
        <div class="typo-first-list">
          <div class="typo-first-item">
            <img src="@/assets/img/typo/1.svg" alt="typo" />
            <!-- <p class="first-item-text text-gradient">The group <span>u</span>niting tec<span>h</span>nologies and
              services for
              di<span>g</span>ital marketing</p> -->
          </div>
          <div class="typo-first-item">
            <img src="@/assets/img/typo/2.svg" alt="typo" />
            <!-- <p class="first-item-text text-dark">The group <span>u</span>niting tec<span>h</span>nologies and services
              for
              di<span>g</span>ital marketing</p> -->
          </div>
          <div class="typo-first-item">
            <img src="@/assets/img/typo/3.svg" alt="typo" />
            <!-- <p class="first-item-text text-white">The group <span>u</span>niting tec<span>h</span>nologies and services
              for
              di<span>g</span>ital marketing</p> -->
          </div>
        </div>
      </div>
      <div class="typo-rule-item typo-rule-second">
        <div class="design-logo-rule typo-rule">
          <span class="rule-num">2</span>
          <p class="rule-text text-second">
            Не используем цветную однородную заливку, так как это не вписывается
            в наш концепт.
          </p>
        </div>
        <div class="typo-first-list">
          <div class="typo-first-item">
            <div class="text-line-through"></div>
            <img
              src="@/assets/img/typo/4.svg"
              alt="typo"
              class=""
            />
            <!-- <p class="first-item-text text-orange text-dark-gradient text-line-through">The group <span>u</span>niting tec<span>h</span>nologies and
              services for
              di<span>g</span>ital marketing</p> -->
          </div>
        </div>
      </div>
      <div class="typo-rule-item typo-rule-third">
        <div class="design-logo-rule typo-rule">
          <span class="rule-num">3</span>
          <p class="rule-text text-second">
            Не используем две акцентные<br />буквы подряд.
          </p>
        </div>
        <div class="typo-first-list">
          <div class="typo-second-item">
            <div class="text-line-through-second"></div>
            <img src="@/assets/img/typo/5.svg" alt="typo" />
            <!-- <p class="second-item-text text-dark-gradient text-line-through"><span>и</span><span>н</span>сайты</p> -->
          </div>
        </div>
      </div>
      <div class="typo-rule-item typo-rule-forth">
        <div class="design-logo-rule typo-rule">
          <span class="rule-num">4</span>
          <p class="rule-text text-second">
            В словах до 13 букв может быть<br />1 акцентная буква.
          </p>
        </div>
        <div class="typo-first-list">
          <div class="typo-second-item">
            <img src="@/assets/img/typo/6.svg" alt="typo" />
            <!-- <p class="second-item-text text-dark-gradient"><span>и</span>нсайты</p> -->
          </div>
        </div>
      </div>
      <div class="typo-rule-item typo-rule-fifth">
        <div class="design-logo-rule typo-rule">
          <span class="rule-num">5</span>
          <p class="rule-text text-second">
            В слове из более чем 13 букв<br />могут быть 2 акцентные буквы.
          </p>
        </div>
        <div class="typo-first-list">
          <div class="typo-second-item typo-second-item-wide">
            <img src="@/assets/img/typo/7.svg" alt="typo" />
            <!-- <p class="second-item-text text-dark-gradient">Р<span>е</span>таргет<span>и</span>нговая</p> -->
          </div>
        </div>
      </div>
    </div>
    <h3 class="text-prime mb-40 mt-120">
      <b>Исключение — сувенирная продукция.</b>
    </h3>
    <p class="text-prime title__text design-logo-wrapper">
      Здесь мы отходим от правил и создаем смелые креативные решения.
    </p>
    <div class="shop-wrapper">
      <img class="shop-item" src="@/assets/img/slides/21.jpg" alt="" />
      <img class="shop-item" src="@/assets/img/slides/22.jpg" alt="" />
    </div>
    <div class="design-color-link mt-120">
      <a
        href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?t=LtdRqYv0NeXV3vrq-0"
        target="_blank"
        class="btn text-prime"
        >Гайд по типографике</a
      >
    </div>
  </div>
</template>
<script>
import TheSwiper from "@/components/TheSwiper.vue";
import {
  eng_alpha,
  ru_alpha,
  num_list,
  sym_list,
  nosym_list,
  sym_list_wide,
} from "@/datas/alphabet";
export default {
  components: {
    TheSwiper,
  },
  computed: {
    eng_alpha() {
      return eng_alpha;
    },
    ru_alpha() {
      return ru_alpha;
    },
    num_list() {
      return num_list;
    },
    sym_list() {
      return sym_list;
    },
    nosym_list() {
      return nosym_list;
    },
    sym_list_wide() {
      return sym_list_wide;
    },
  },
  data() {
    return {
      items: [
        { content: 11, width: 305 },
        { content: 12, width: 650 },
        { content: 13, width: 402 },
        { content: 14, width: 718 },
      ],
    };
  },
};
</script>
<style lang="scss">
@use "@/assets/scss/abstracts" as *;

.font-wrapper {
  max-width: 1030px;
  width: 100%;
  margin: 0 auto;
}

.alphabet-wrapper {
  @include flex(row, space-between, stretch);
}

.alpha-item {
  background: $white;
  width: 100%;
  border: 1px solid $black;
  padding: 45px 75px;
  user-select: none;

  &__dark {
    background: $black;
    color: $white;
  }
}

.alpha-list {
  @include flex(row, start);
  flex-wrap: wrap;
  gap: 10px 35px;

  &-slim {
    @include flex(row, space-between);
    gap: 0;
  }

  &-small {
    gap: 10px 23px;
  }
}

.alpha-letter {
  font-weight: 400;
  transition: 0.3s;
  cursor: pointer;

  &:hover {
    opacity: 0.3;
  }

  &-up {
    text-transform: uppercase;
  }

  &-wide {
    font-size: 34px;
  }

  &-slim {
    font-size: 25px;
  }
}

.alpha-symbol {
  margin-left: 10px;
}

.typo-rules {
  @include flex(row, start);
  flex-wrap: wrap;
  gap: 10px 120px;

  .typo-rule {
    max-width: 600px;
  }
}

.typo-rule-item {
  max-width: 612px;
}

.typo-rule-first {
  max-width: 100%;
}

.typo-rule-second,
.typo-rule-forth {
  max-width: 507px;
}

.typo-first-list {
  margin: 35px 0 85px;
  @include flex(row, space-between);
  gap: 16px;
}

.typo-first-item {
  background: $light-black;
  border: 1px solid $black;
  color: $white;
  padding: 60px 53px;
  max-width: 403px;
  position: relative;
}

.first-item-text {
  font-weight: 600;
  font-size: 30px;
  position: relative;
  span {
    font-family: "Robtronika";
    font-size: 22px;
  }

  &.text-dark span {
    text-shadow: -1px 0 $white, 0 1px $white, 1px 0 $white, 0 -1px $white;
    color: $black;
  }

  &.text-gradient span {
    background: linear-gradient(90deg, $white 39.31%, $orange 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-fill-color: transparent;
  }

  &.text-orange span {
    color: $orange;
  }
}
.text-line-through {
    &::after {
      content: "";
      position: absolute;
      width: 100%;
      height: 2px;
      background: $red;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-35deg);
    }
  }
.second-item-text {
  font-size: 54px;
  font-weight: 600;
  position: relative;

  span {
    font-family: "Robtronika";
    font-size: 40px;
  }

  &.text-line-through {
    &::after {
      content: "";
      position: absolute;
      width: 70%;
      height: 2px;
      background: $red;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-15deg);
    }
  }

  &.text-dark-gradient span {
    background: linear-gradient(90deg, $black 39.31%, $orange 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-fill-color: transparent;
  }
}

.typo-second-item {
  background: $white;
  border: 1px solid $black;
  color: $black;
  padding: 65px;
  max-width: 507px;
  width: 100%;
  text-align: center;
  font-size: 54px;
position: relative;
  &-wide {
    max-width: 100%;
  }
}
.text-line-through-second {
    &::after {
      content: "";
      position: absolute;
      width: 80%;
      height: 2px;
      background: $red;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-15deg);
    }
  }
.shop-wrapper {
  margin-top: 80px;
  @include flex(row, center, center);
}

.shop-item {
  max-width: 400px;
  width: 100%;
  cursor: pointer;
}
</style>
