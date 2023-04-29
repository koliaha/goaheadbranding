<template>
  <nav class="nav">
    <div class="container">
      <div class="nav-list">
        <div class="dropdown">
          <router-link class="nav-item" exact-active-class="active" to="/" @click="scrollto('','brand')">
            Бренд
          </router-link>
          <div class="dropdown-content text-prime"  v-if="isNavbarSticky">
            <div class="dropdown-list asp">
              <a @click="scrollto('','mission')">Наша миссия</a>
              <a @click="scrollto('','target')">Наши ценности</a>
            </div>
          </div>
        </div>
        <div class="dropdown">
          <router-link
            class="nav-item"
            exact-active-class="active"
            to="/content"
            @click="scrollto('content','brand')"
          >
            Контент
          </router-link>
          <div class="dropdown-content text-prime" v-if="isNavbarSticky">
            <div class="dropdown-list asp">
              <a @click="scrollto('content','tone')">Tone of voice</a>
              <a @click="scrollto('content','audio')">Аудитория</a>
              <a @click="scrollto('content','units')">Написание юнитов</a>
            </div>
          </div>
        </div>
        <div class="dropdown">
          <router-link
            class="nav-item"
            exact-active-class="active"
            to="/design"
            @click="scrollto('design','brand')"
          >
            Дизайн
            <div class="arrow-down"></div>
          </router-link>
          <div class="dropdown-content text-prime"  v-if="isNavbarSticky">
            <div class="dropdown-list dsp">
              <a @click="scrollto('design','logo')">Логотип</a>
              <a @click="scrollto('design','unit')">Написание юнитов</a>
              <a @click="scrollto('design','color')">Цвет</a>
              <a @click="scrollto('design','bg')">Фоны</a>
              <a @click="scrollto('design','type')">Типографика</a>
              <a @click="scrollto('design','pattern')">Паттерны</a>
              <a @click="scrollto('design','presentations')">Презентация</a>
              <a @click="scrollto('design','smm')">SMM</a>
              <a @click="scrollto('design','ban')">Баннеры</a>
              <a @click="scrollto('design','imidge')">Имиджи</a>
              <a @click="scrollto('design','merch')">Мерч и наружная реклама</a>
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
  data() {
    return {
      isNavbarSticky: false,
    };
  },
  methods: {
    scrollto(route,id) {
      // if (this.currentRouteName != "/design") {
        this.$router.push({ path: `/${route}` });
        setTimeout(() => {
          const el = document.getElementById(id);
          el.scrollIntoView({ behavior: "smooth" });
        }, 500);
        // return;
      // }
      // const el = document.getElementById(id);
      // el.scrollIntoView({ behavior: "smooth" });
    },
    handleScroll() {
      const fixedOffset = 500;
      this.isNavbarSticky = window.scrollY >= fixedOffset;
    },
  },
  computed: {
    currentRouteName() {
      return this.$route.path;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>
