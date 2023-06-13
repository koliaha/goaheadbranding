<template>
  <div class="container">
    <h1 class="text-title">Имиджи</h1>
    <p class="text-prime title__text">Мы используем следующие типы имиджей:</p>
    <ul class="text-prime">
      <li>3D</li>
      <li>Коллаж</li>
      <li>Фотографии</li>
    </ul>
    <p class="text-prime title__text design-logo-wrapper">
      С подробными правилами и примерами вы можете ознакомиться в нашем гайде в
      фигме
    </p>
    <h3 class="text-prime mb-40 text-center"><b>Примеры имиджей</b></h3>
    <TheSwiper :list-image="items" />
    <p class="text-prime title__text mt-120 mb-40">
    </p>
    <div class="design-color-link mt-120">
      <a
        href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?type=design&node-id=694%3A3576&t=BjHwnqNYH59gVC0K-1"
        target="_blank"
        class="btn text-prime"
        >Гайд по имиджам</a
      >
      <a
        href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?type=design&node-id=3277-3631&t=pRLKLv2btESRinUF-0"
        target="_blank"
        class="btn btn-light text-prime mx-30"
        >Фирменные 3д</a
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
        { content: 71, width: 402 },
        { content: 72, width: 402 },
        { content: 73, width: 402 },
        { content: 74, width: 402 },
        { content: 75, width: 402 },
        { content: 76, width: 402 },
      ],
    };
  },
};
</script>
<style lang="scss">
.design-imidge-link {
  margin: 20px 0;
  a {
    margin: 15px 0;
  }
}
</style>
