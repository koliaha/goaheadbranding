<template>
    <header class="header header-brand">
        <div class="brand-circle brand-circle-first">
            <img class="brand-circle-img" src="@/assets/img/bg/circle.svg" alt="">
        </div>
        <div class="brand-circle brand-circle-second">
            <img class="brand-circle-img" src="@/assets/img/bg/circle2.svg" alt="">
        </div>
        <div class="header-content">
            <div class="header-content__logo">
                <!-- <img src="@/assets/img/logo.svg" alt="logo" class="header-content__img"> -->
                <div class="header-content__logo-title"><span>go</span>ahead</div>
            </div>
            <div class="header-content__title">Бр<span class="robo">Е</span>нд</div>
            <div class="header-content__subtitle text-second">
                <div class="header-content__subtitle-item" @click="scrollto('mission')">Наша миссия</div>
                <div class="header-content__subtitle-item" @click="scrollto('price')">Наши ценности</div>
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