<template>
    <div class="swiper-custom">
        <swiper :slidesPerView="slidePerpage || 3" :spaceBetween="25" :navigation="true" :modules="modules" loop="true"
        :breakpoints="{
              768: {
                slidesPerView: 2,
              },
              1070: {
                slidesPerView: `${slidePerpage || 3}`,
              },
            }" class="mySwiper">
            <swiper-slide class="swiper-image" v-for="(i, index) in listImage" :key="index" :class="[isWide?.includes(index) && 'wide'] || ''">
                <img :src="getImgUrl(i)" alt="slides">
            </swiper-slide>
        </swiper>
    </div>
</template>
<script>
import { Navigation } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/scrollbar';
export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    props: ["listImage", "slidePerpage","isWide"],
    setup() {
        const getImgUrl = (id) => {
            const images = require.context('@/assets/img/slides/', false, /\.jpg$/)
            return images('./' + id + ".jpg")
        }
        return {
            modules: [Navigation],
            getImgUrl
        };
    },
};
</script>
<style lang="scss">
@use "@/assets/scss/abstracts" as *;
.swiper-image {
    height: 402px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 35px 0 !important;
    img {
        display: block;
        height: 100%;
    }
}
.swiper-image.wide {
    max-width: 725px !important;
    width: 100% !important;
}
.swiper-custom {
    .swiper{
        padding-bottom: 40px;
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
        &::after{
        font-size: 22px;
        }
    }
    .swiper-button-prev{
        left: 45%;
        padding-right: 5px;
    }
    .swiper-button-next{
        right: 45%;
        padding-left: 5px;
    }
}
</style>