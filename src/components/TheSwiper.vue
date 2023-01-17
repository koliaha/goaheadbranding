<template>
    <div class="swiper-custom">
        <swiper :slidesPerView="slidePerpage || 3" :spaceBetween="15" :loop="true" :navigation="true" :modules="modules" class="mySwiper">
            <swiper-slide class="swiper-image" v-for="(i, index) in listImage" :key="index">
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
    props: ["listImage", "slidePerpage"],
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
    margin: 35px 0;

    img {
        display: block;
        height: 100%;
    }
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