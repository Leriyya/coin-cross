<template>
    <div class="card-choose">
        <img :src="image" alt="Card" class="cardChoose__image" />
        <div class="card-choose__content">
            <div class="card-choose__title">{{ title }}</div>
            <div class="card-choose__text">{{ text }}</div>
        </div>

    </div>
</template>
  
<script>
export default {
    props: {
        image: {
            type: String,
            required: true,
        },
        title: {
            type: String,
            required: true,
        },
        text: {
            type: String,
            required: true,
        },
    },
};
</script>
  
<style lang="scss" scoped>
.card-choose {
    border-radius: 24px;
    padding: 36px 32px;
    margin-bottom: 16px;
    background-color: var(--white);
    width: 100%;

    @media (max-width: 1020px) {
        padding: 26px 25px;
    }

   
    @media (max-width: 700px) {
        width: auto;
    }

    &__image {
        margin-bottom: 50px;

        @media (max-width: 1020px) {
            margin-bottom: 10px;
        }
    }

    &__title {
        color: #16161C;
        font-size: 24px;
        margin-bottom: 16px;
    }

    &__text {
        font-size: 16px;
        color: var(--dark-grey);

        @media (max-width: 1020px) {
            font-size: 14px;
        }
    }

}
</style>