<script setup>
import CardWhy from './CardWhy.vue';

</script>

<template>
    <div class="why">
        <div class="why__container">
            <div class="why__title">Почему выбирают нас?</div>
            <div class="why__cardsContainer">
                <div class="why__img"><img src="@/assets/svg/whywe.svg" alt=""></div>
                <div class="why__cards">
                    <CardWhy image="src/assets/svg/crown.svg" title="100% гарантия"
                        text="Наша команда готова решить любые проблемы и ответить на ваши вопросы в чате поддержки" />
                    <CardWhy image="src/assets/svg/pig.svg" title="Экономичный обмен "
                        text="Предлагаем самый выгодный обмен валюты на рынке для наших клиентов" />
                    <CardWhy image="src/assets/svg/B.svg" title="Множество вариантов"
                        text="Обменивайте десятки видов электронных валют и узнавайте их стоимость в реальном времени" />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.why {
    padding-top: 90px;
    padding-bottom: 80px;
    background-color: var(--light-grey);

    @media (max-width: 1020px) {
        padding-top: 10px;
    }

    &__container {
        max-width: 1180px;
        margin: 0 auto;
        padding: 0 20px;
    }

    &__cards {
        display: flex;
        gap: 48px;

        @media (max-width: 1070px) {
            gap: 15px;
        }

        @media (max-width: 1020px) {
            flex-direction: column;
        }
    }

    &__title {
        color: #16161C;
        font-size: 52px;
        font-weight: 700;
        text-align: center;

        @media (max-width: 1020px) {
            font-size: 32px;
        }
    }

    &__cardsContainer {
        margin-top: 64px;

        @media (max-width: 1020px) {
            margin-top: 24px;
        }
    }

    &__img {
        background-color: #F0F0F0;
        border-radius: 24px;
        margin-bottom: 48px;

        img {
            margin-bottom: -7px
        }

        @media (max-width: 1130px) {
            img {
                width: 100%;
            }
        }
        @media (max-width: 1020px) {
            margin-bottom: 20px;
        }
    }
}
</style>