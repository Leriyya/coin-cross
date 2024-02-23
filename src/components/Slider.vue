<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import SwiperCore from 'swiper';
import { Pagination } from 'swiper/modules';
import Card from '@/components/CardShare.vue';
import 'swiper/css';
import 'swiper/css/pagination';

SwiperCore.use([Pagination]);

export default {
    components: {
        Swiper,
        SwiperSlide,
        Card,
    },

    setup() {
        return {
            modules: [Pagination],
            pagination: {
                clickable: true,
                renderBullet: function (index, className) {
                    return '<span class="slider__paginatione ' + className + '"> </span>';

                }
            }
        };
    },
};
</script>

<template>
    <Swiper style="--swiper-pagination-color: #FFBA08" :slides-per-view="1" :space-between="50" @swiper="onSwiper"
        @slideChange="onSlideChange" class="slider" :pagination="pagination">
        <SwiperSlide class="slider__slide">
            <Card image="src/assets/svg/tg.svg" text="Присоединяйтесь к нашему " text2="Telegram-каналу CoinCross" />
        </SwiperSlide>
        <SwiperSlide class="slider__slide">
            <Card image="src/assets/svg/review.svg" text="Оставьте свой отзыв на платформе — " text2="выиграй 30 USDT" />
        </SwiperSlide>
        <SwiperSlide class="slider__slide">
            <Card image="src/assets/svg/advert.svg" text="Рекламируйте свой криптопроект с " text2="Good Marketing" />
        </SwiperSlide>
    </Swiper>
</template>



<style lang="scss" scoped>
.slider {
    @media (min-width: 1000px) {
        display: none;
    }

    padding-top: 30px;
    background-color: var(--light-grey);
    overflow-y: visible;


}
</style>