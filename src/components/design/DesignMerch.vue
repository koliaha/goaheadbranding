<template>
  <div class="container">
    <h1 class="text-title">Мерч и наружная реклама</h1>
    <h3 class="text-prime mb-40 text-center mt-120"><b>Примеры</b></h3>
   
  </div>
  <TheSwiper
      :list-image="[21, 22, 23]"
      :slide-perpage="3"
    />
</template>
<script>
import TheSwiper from "@/components/TheSwiper.vue";
export default {
  components: {
    TheSwiper,
  },
};
</script>
