<template>
  <div id="app">
    <NavBar/>
    <router-view />
    <TheFooter/>
  </div>
</template>
<script>
import NavBar from '@/components/NavBar.vue'
import TheFooter from '@/components/TheFooter.vue'
export default {
  components: {
    NavBar,TheFooter
  }
}
</script>
<style lang="scss">
@import '@/assets/scss/index.scss';
</style>

