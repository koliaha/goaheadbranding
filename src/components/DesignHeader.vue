<template>
  <header class="header header-brand">
    <div class="brand-circle brand-circle-eighth">
      <img class="brand-circle-img" src="@/assets/img/bg/circle8.svg" alt="">
    </div>
    <div class="brand-circle brand-circle-ninth">
      <img class="brand-circle-img" src="@/assets/img/bg/circle9.svg" alt="">
    </div>
    <div class="brand-circle brand-circle-tenth">
      <img class="brand-circle-img" src="@/assets/img/bg/circle10.svg" alt="">
    </div>
    <div class="header-content">
      <div class="header-content__logo">
        <!-- <img src="@/assets/img/logo.svg" alt="logo" class="header-content__img"> -->
        <div class="header-content__logo-title"><span>go</span>ahead</div>
      </div>
      <div class="header-content__title">Д<span class="robo">и</span>зайн</div>
      <div class="header-content__subtitle text-second">
        <div class="header-content__subtitle-item" @click="scrollto('logo')">Логотип</div>
        <div class="header-content__subtitle-item" @click="scrollto('color')">Цвет</div>
        <div class="header-content__subtitle-item" @click="scrollto('unit')">Написание юнитов</div>
        <div class="header-content__subtitle-item" @click="scrollto('type')">Типографика</div>
        <div class="header-content__subtitle-item" @click="scrollto('pattern')">Паттерны</div>
        <div class="header-content__subtitle-item" @click="scrollto('presentations')">Презентация</div>
        <div class="header-content__subtitle-item" @click="scrollto('smm')">SMM</div>
        <div class="header-content__subtitle-item" @click="scrollto('ban')">Баннеры</div>
        <div class="header-content__subtitle-item" @click="scrollto('imidge')">Имиджи</div>
        <div class="header-content__subtitle-item" @click="scrollto('merch')">Мерч и наружная реклама</div>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  name: "BrandHeader",
  methods: {
    scrollto(id) {
      const el = document.getElementById(id);
      el.scrollIntoView({ behavior: "smooth" });
    },
  },
  computed: {
    currentRouteName() {
      return this.$route.path;
    },
  },
};
</script>