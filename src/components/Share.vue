<script setup>
import Card from '@/components/CardShare.vue';
</script>

<template>
    <div class="share">
        <div class="share__container">
            <Card image="src/assets/svg/tg.svg" text="Присоединяйтесь к нашему " text2="Telegram-каналу CoinCross" />
            <Card image="src/assets/svg/review.svg" text="Оставьте свой отзыв на платформе — " text2="выиграй 30 USDT" />
            <Card image="src/assets/svg/advert.svg" text="Рекламируйте свой криптопроект с " text2="Good Marketing" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.share {
    padding-top: 44px;
    background-color: #f9f8f8;

    @media (max-width: 1000px) {
        display: none;
    }

    &__container {
        max-width: 1180px;
        margin: 0 auto;
        padding: 0 2rem;
        display: flex;
        justify-content: space-evenly;
        gap: 48px;

        @media (max-width: 1130px) {
            gap: 20px;
        }
    }
}
</style>