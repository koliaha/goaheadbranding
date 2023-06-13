<template>
  <div class="swiper-custom container wide">
    <!-- :breakpoints="{
        768: {
          slidesPerView: 2,
        },
        1070: {
          slidesPerView: `${slidePerpage || 3}`,
        },
      }" -->
      <!-- :centeredSlides="true" -->

    <swiper
      slidesPerView="auto"
      :spaceBetween="120"
      :navigation="true"
      :modules="modules"
      :initialSlide="0"
      class="mySwiper"
      :loop="loop"
    >
    <!-- :class="[isWide?.includes(index) && 'wide'] || ''" -->

      <swiper-slide
        class="swiper-image"
        v-for="(i, index) in listImage"
        :key="index"
        :style="{width: i?.width + 'px'}"
      >
        <img :src="getImgUrl(i?.content)" alt="slides" />
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
import { Navigation } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/scrollbar";
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props: ["listImage", "slidePerpage", "isWide","loop"],
  setup() {
    const getImgUrl = (id) => {
      const images = require.context("@/assets/img/slides/", false, /\.jpg$/);
      return images("./" + id + ".jpg");
    };
    return {
      modules: [Navigation],
      getImgUrl,
    };
  },
};
</script>
<style lang="scss">
@use "@/assets/scss/abstracts" as *;
.swiper-image {
//   display: flex;
//   justify-content: center;
//   align-items: center;
//   margin: 35px 0 !important;
user-select: none;
  img {
    // display: block;
    // height: 100%;
  height: 402px;
  }
}
.swiper-image.wide {
  max-width: 725px !important;
  width: 100% !important;
}
.swiper-custom {
  .swiper {
    padding-bottom: 80px;
    overflow: visible;
  }
  .swiper-button-next,
  .swiper-button-prev {
    top: auto;
    bottom: 0px;
    z-index: 100;
    width: 40px;
    height: 40px;
    background: $white;
    border-radius: 50%;
    border: 1px solid $black;
    color: $black;
    &::after {
      font-size: 22px;
    }
  }
  .swiper-button-prev {
    left: 45%;
    padding-right: 5px;
  }
  .swiper-button-next {
    right: 45%;
    padding-left: 5px;
  }
}
</style>
