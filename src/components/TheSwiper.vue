<template>
    <swiper :slidesPerView="2" :spaceBetween="30" :centeredSlides="true" :pagination="{
    clickable: true,
}" :modules="modules" class="mySwiper">
        <swiper-slide class="swiper-image" v-for="(i, index) in listImage" :key="index">
            <img :src="getImgUrl(i)" alt="slides">
        </swiper-slide>
    </swiper>
</template>
<script>
import { Pagination } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    props:["listImage"],
    setup() {
        const getImgUrl=(id)=> {
            const images = require.context('@/assets/img/slides/', false, /\.jpg$/)
            return images('./' + id + ".jpg")
        }
        return {
            modules: [Pagination],
            getImgUrl
        };
    },
};
</script>
<style lang="scss">
.swiper-image {
    height: 402px;
    display: flex;
    justify-content: center;
    align-items: center;

    img {
        display: block;
        height: 100%;
    }
}
</style>