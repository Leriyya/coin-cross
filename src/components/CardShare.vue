<template>
    <div class="card">
        <div class="card__content">
            <div class="card__text">{{ text }}<span class="card__subText">{{ text2 }}</span></div>
        </div>
        <img :src="image" alt="Card Image" class="card__image" />
    </div>
</template>
  
<script>
export default {
    props: {
        image: {
            type: String,
            required: true,
        },
        text: {
            type: String,
            required: true,
        },
        text2: {
            type: String,
            required: true,
        },
    },
};
</script>
  
<style lang="scss" scoped>
.card {
    border: 1px solid #ccc;
    border-radius: 24px;
    border: none;
    padding-top: 18px;
    padding-left: 16px;
    margin-bottom: 16px;
    background-color: var(--white);
    display: flex;
    justify-content: space-between;
    gap: 35px;

    @media (max-width: 1130px) {
        gap: 10px;
    }

    @media (max-width: 1000px) {
        width: 509px;
        margin: auto;
        height: 164px;
    }

    @media (max-width: 700px) {
        width: 300px;
        height: 100px;
    }

    &__image {
        @media (max-width: 1130px) {
            width: 100%;
        }

        @media (max-width: 1000px) {
            width: 244px
        }

        @media (max-width: 700px) {
            width: 100px;
        }
    }

    &__text {
        font-size: 16px;
    }

    &__subText {
        color: #FE7F32;
        font-size: 16px;
        font-style: italic;
    }
}
</style>