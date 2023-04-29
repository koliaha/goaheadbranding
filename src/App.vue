<template>
  <div id="app">
    <NavBar ref="navbar" class="nav-header" :class="{ 'fixed-navbar': isNavbarSticky }"/>
    <router-view />
    <TheFooter />
  </div>
</template>
<script>
import NavBar from "@/components/NavBar.vue";
import TheFooter from "@/components/TheFooter.vue";
export default {
  components: {
    NavBar,
    TheFooter,
  },
  data() {
    return {
      isNavbarSticky: false,
    };
  },
  methods: {
    handleScroll() {
      const fixedOffset = 600;
      this.isNavbarSticky = window.scrollY >= fixedOffset;
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
<style lang="scss">
@import "@/assets/scss/index.scss";
.nav-header{
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  transition: top 1s ease-in-out;
}
.fixed-navbar {
  position: fixed;
  top: 0;
  z-index: 100;
  background: #262626;
}
</style>
