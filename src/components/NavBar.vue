<template>
  <nav class="nav">
    <div class="container">
      <div class="nav-list">
        <router-link class="nav-item" exact-active-class="active" to="/"
          >Бренд</router-link
        >
        <router-link class="nav-item" exact-active-class="active" to="/content"
          >Контент</router-link
        >
        <div class="dropdown">
          <router-link class="nav-item" exact-active-class="active" to="/design"
            >Дизайн
            <div class="arrow-down"></div
          ></router-link>
          <div class="dropdown-content text-prime">
            <div class="dropdown-list dsp">
              <a @click="scrollto('logo')">Логотип</a>
              <a @click="scrollto('unit')">Написание юнитов</a>
              <a @click="scrollto('color')">Цвет</a>
              <a @click="scrollto('bg')">Фоны</a>
              <a @click="scrollto('type')">Типографика</a>
              <a @click="scrollto('pattern')">Паттерны</a>
              <a @click="scrollto('presentations')">Презентация</a>
              <a @click="scrollto('smm')">SMM</a>
              <a @click="scrollto('banners')">Баннеры</a>
              <a @click="scrollto('imidge')">Имиджи</a>
              <a @click="scrollto('merch')">Мерч и наружная реклама</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  name: "navBar",
  methods: {
    scrollto(id) {
      if (this.currentRouteName != "/design") {
        this.$router.push({ path: "/design" });
        setTimeout(() => {
          const el = document.getElementById(id);
      el.scrollIntoView({ behavior: "smooth" });
        }, 500);
        return;
      }
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
