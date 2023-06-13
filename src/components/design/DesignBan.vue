<template>
  <div class="container">
    <h1 class="text-title">Баннеры</h1>
    <p class="text-prime title__text">
      Все правила и шаблоны вы найдете в гайде по баннерам
    </p>
    <h3 class="text-prime mb-40 text-center mt-120"><b>Примеры баннеров</b></h3>
    <TheSwiper :list-image="items" :slide-perpage="2" />
    <div class="design-color-link mt-120">
      <a
        href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?type=design&node-id=677%3A3071&t=gei2ecgKVrsMXu0G-1"
        target="_blank"
        class="btn text-prime"
        >Гайд по баннерам</a
      >
    </div>
  </div>
</template>
<script>
import TheSwiper from "@/components/TheSwiper.vue";
export default {
  components: {
    TheSwiper,
  },
  data() {
    return {
      items: [
        { content: 61, width: 715 },
        { content: 62, width: 715 },
        { content: 33, width: 715 },
      ],
    };
  },
};
</script>
