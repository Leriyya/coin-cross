<script setup>
import Transaction from './Transaction.vue';
</script>

<template>
    <div class="history">
        <div class="history__container">
            <div class="history__title">Последние обмены</div>
            <div class="history__transactions">
                <Transaction imageGive="src/assets/svg/tickets1.svg" imageRecieve="src/assets/svg/tickets2.svg"
                    timeAgo="10 минут" seconds="10 секунд" coinGiveName="DAI (DAI)" coinGivePrice="435,423"
                    coinRecieveName="Сбербанк (RUB)" coinRecievePrice="39 096,63" />
                <Transaction imageGive="src/assets/svg/tickets1.svg" imageRecieve="src/assets/svg/tickets2.svg"
                    timeAgo="10 минут" seconds="10 секунд" coinGiveName="DAI (DAI)" coinGivePrice="435,423"
                    coinRecieveName="Сбербанк (RUB)" coinRecievePrice="39 096,63" />
                <Transaction imageGive="src/assets/svg/tickets1.svg" imageRecieve="src/assets/svg/tickets2.svg"
                    timeAgo="10 минут" seconds="10 секунд" coinGiveName="DAI (DAI)" coinGivePrice="435,423"
                    coinRecieveName="Сбербанк (RUB)" coinRecievePrice="39 096,63" />
                <Transaction imageGive="src/assets/svg/tickets1.svg" imageRecieve="src/assets/svg/tickets2.svg"
                    timeAgo="10 минут" seconds="10 секунд" coinGiveName="DAI (DAI)" coinGivePrice="435,423"
                    coinRecieveName="Сбербанк (RUB)" coinRecievePrice="39 096,63" />
            </div>
            <button class="history__update">Обновить список (2)</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.history {
    padding-top: 160px;
    padding-bottom: 40px;
    background-color: #f9f8f8;

    @media (max-width: 1020px) {
        padding-top: 80px;
    }

    &__container {
        max-width: 1180px;
        margin: 0 auto;
        padding: 0 2rem;
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

    &__transactions {
        padding-top: 64px;
        display: flex;
        flex-direction: column;
        gap: 24px;

        @media (max-width: 1020px) {
            padding-top: 24px;
        }
    }

    &__update {
        border: 1px solid #FE7F32;
        border-radius: 12px;
        background: transparent;
        color: #FE7F32;
        font-size: 16px;
        padding: 12px 24px;
        display: flex;
        margin: 32px auto;
        cursor: pointer;
    }
}
</style>