<template>
    <header class="header header-brand">
      <div class="brand-circle brand-circle-tringle">
        <img class="brand-circle-img" src="@/assets/img/bg/tringle.svg" alt="">
      </div>
      <div class="brand-circle brand-circle-tringle2">
        <img class="brand-circle-img" src="@/assets/img/bg/tringle2.svg" alt="">
      </div>
        <div class="header-content">
            <div class="header-content__logo">
                <!-- <img src="@/assets/img/logo.svg" alt="logo" class="header-content__img"> -->
                <div class="header-content__logo-title"><span>go</span>ahead</div>
            </div>
            <div class="header-content__title">Конт<span class="robo">Е</span>нт</div>
            <div class="header-content__subtitle text-second">
                <div class="header-content__subtitle-item" @click="scrollto('tone')">Tone of voice</div>
                <div class="header-content__subtitle-item" @click="scrollto('audio')">Аудитория</div>
                <div class="header-content__subtitle-item" @click="scrollto('units')">Написание юнитов</div>
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