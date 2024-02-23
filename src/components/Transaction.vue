<template>
    <div class="transaction">
        <div class="transaction__change">
            <div class="transaction__coinContainer">
                <img :src="imageGive" alt="coin" class="transaction__coin" />
                <div>
                    <div class="transaction__coinName">{{ coinGiveName }}</div>
                    <div class="transaction__coinPrice">{{ coinGivePrice }}</div>
                </div>
            </div>
            <div><img src="@/assets/svg/change-black.svg" alt=""></div>
            <div class="transaction__coinContainer">
                <img :src="imageRecieve" alt="coin" class="transaction__coin" />
                <div>
                    <div class="transaction__coinName">{{ coinRecieveName }}</div>
                    <div class="transaction__coinPrice">{{ coinRecievePrice }}</div>
                </div>
            </div>
        </div>
        <div class="transaction__time">
            <div class="transaction__seconds"><img src="@/assets/svg/clock.svg" alt="">{{ seconds }}</div>
            <div class="transaction__timeAgo">{{ timeAgo }} назад</div>
        </div>
    </div>
</template>
  
<script>
export default {
    props: {
        imageGive: {
            type: String,
            required: true,
        },
        imageRecieve: {
            type: String,
            required: true,
        },
        timeAgo: {
            type: String,
            required: true,
        },
        seconds: {
            type: String,
            required: true,
        },
        coinGiveName: {
            type: String,
            required: true,
        },
        coinGivePrice: {
            type: String,
            required: true,
        },
        coinRecieveName: {
            type: String,
            required: true,
        },
        coinRecievePrice: {
            type: String,
            required: true,
        },
    },
};
</script>
  
<style lang="scss" scoped>
.transaction {
    background-color: var(--white);
    padding: 16px 32px;
    border-radius: 24px;
    display: flex;
    justify-content: space-between;

    @media (max-width: 1020px) {
        flex-direction: column;
    }
    @media (max-width: 700px) {
        padding: 10px;
        box-shadow: 0px 4px 20px 0px #4A4A4A12;
    }

    &__change {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 50%;

        @media (max-width: 1020px) {
            width: 100%;
        }
    }

    &__coinContainer {
        display: flex;
        gap: 8px;
        align-items: center;
    }

    &__time {
        display: flex;
        align-items: center;
        gap: 20px;

        @media (max-width: 1020px) {
            justify-content: space-between;
            margin-top: 14px;
        }
    }

    &__coinName {
        color: #16161C;
        font-size: 16px;

        @media (max-width: 700px) {
            font-size: 14px;
        }
    }

    &__coinPrice {
        color: var(--dark-grey);
        font-size: 14px;

        @media (max-width: 700px) {
            font-size: 12px;
        }
    }

    &__seconds {
        display: flex;
        color: #868686;
        font-size: 14px;
        align-items: center;
        gap: 5px;

        @media (max-width: 700px) {
            font-size: 12px;
        }
    }

    &__timeAgo {
        color: #D6D6D6;
        font-size: 14px;

        @media (max-width: 700px) {
            font-size: 12px;
        }
    }
}
</style>