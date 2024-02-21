<script>
export default {
    data() {
        return {
            isDropdownOpen: false,
            selectedOption: 'ETH Ether',
            options: [
                { id: 1, label: 'Опция 1' },
                { id: 2, label: 'Опция 2' },
                { id: 3, label: 'Опция 3' },
            ],
            inputValue: '',
        };
    },
    methods: {
        toggleDropdown() {
            this.isDropdownOpen = !this.isDropdownOpen;
        },
        selectOption(option) {
            this.selectedOption = option.label;
            this.isDropdownOpen = false;
        },
    },
};
</script>

<template>
    <div class="exchanger">
        <div class="exchanger__container">
            <div class="exchanger__title">Короли на рынке криптообмена</div>
            <div class="exchanger__subTitle">Надежно, быстро, анонимно</div>
            <div class="exchanger__form">
                <div class="exchanger__formChange">
                    <div class="exchanger__give">
                        <div class="exchanger__name">Вы отдаете</div>
                        <div>
                            <button class="exchanger__dropdownToggle" @click="toggleDropdown">
                                <div><img src="../assets/svg/tickets.svg" />{{ selectedOption }}</div> <img
                                    src="../assets/svg/arrow-down.svg" />
                            </button>
                            <input type="text" v-model="inputValue" class="exchanger__input" placeholder="1" />
                        </div>

                    </div>
                    <div class="exchanger__icon"><img src="../assets/svg/change.svg" alt=""></div>
                    <div class="exchanger__recieve">
                        <div class="exchanger__name">Вы получаете</div>
                        <div>
                            <button class="exchanger__dropdownToggle" @click="toggleDropdown">
                                <div><img src="../assets/svg/tickets1.svg" />DAI Dai</div> <img
                                    src="../assets/svg/arrow-down.svg" />
                            </button>
                            <input type="text" v-model="inputValue" class="exchanger__input" placeholder="2 267,24" />
                        </div>

                    </div>
                </div>
                <div class="exchanger__formBottomInfo">
                    <div class="exchanger__formInfo">
                        <div class="exchanger__formCourse">
                            <div>Курс: 1 USDT = 69,06 RUB </div>
                            <div class="exchanger__logo"><img src="../assets/svg/logo.svg" alt=""></div>
                        </div>
                        <div class="exchanger__formSubInfo">
                            <div class="exchanger__formTime"><img src="../assets/svg/clock.svg" alt="">Время обмена до
                                60
                                минут</div>
                            <div class="exchanger__formReserve">
                                <div class="exchanger__reserve"><img src="../assets/svg/coins.svg" alt="">Резерв 12 324
                                    DAI</div>
                                <button>Не хватает?</button>
                            </div>
                        </div>
                    </div>
                    <div class="exchanger__continue">
                        <button>Продолжить</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.exchanger {
    padding-top: 64px;
    padding-bottom: 126px;
    background-color: #f9f8f8;
    background: linear-gradient(to bottom, #f9f8f8 50%, #F0F0F0 50%);

    @media (max-width: 700px) {
        padding-bottom: 60px;
    }

    &__container {
        max-width: 1180px;
        margin: 0 auto;
        padding: 0 2rem;
    }

    &__reserve {
        display: flex;
        align-items: center;
        gap: 5px;
    }

    &__logo {
        img {
            width: 142px;
        }

        @media (max-width: 700px) {
            display: none;
        }
    }

    &__title {
        font-size: 52px;
        font-weight: 700;
        color: #16161C;
        margin-bottom: 20px;
        text-align: center;

        @media (max-width: 1020px) {
            font-size: 32px;
            line-height: 40px;
            margin-bottom: 15px;
        }
    }

    &__subTitle {
        font-size: 24px;
        font-weight: 400;
        text-align: center;
        color: #585858;

        @media (max-width: 1020px) {
            font-size: 16px;
        }
    }

    &__icon {
        margin-top: 80px;

        @media (max-width: 1020px) {
            margin-top: 14px;
        }
    }

    &__form {
        display: flex;
        margin-top: 42px;
        background-color: white;
        border-radius: 24px;
        padding: 32px;
        flex-direction: column;
    }

    &__formChange {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;

        @media (max-width: 1020px) {
            flex-direction: column;
            gap: 10px;
        }
    }

    &__formBottomInfo {
        display: flex;
        justify-content: space-between;

        @media (max-width: 1020px) {
            flex-direction: column;
        }
    }

    &__give,
    &__recieve {
        width: 45%;

        @media (max-width: 1020px) {
            width: 100%;
        }
    }


    &__name {
        color: #585858;
        font-size: 24px;
        font-weight: 400;
        margin-bottom: 24px;
    }

    &__dropdownToggle {
        background-color: #FFF9F5;
        border: 1px solid #FE7F3226;
        border-radius: 16px;
        padding: 12px 24px;
        font-size: 24px;
        display: flex;
        align-items: center;
        width: 100%;
        justify-content: space-between;
        margin-bottom: 24px;
        cursor: pointer;

        div {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        @media (max-width: 700px) {
            width: 100%;

        }
    }

    &__input {
        background-color: #FFF9F5;
        border: 1px solid #FE7F3226;
        border-radius: 16px;
        padding: 12px 24px;
        font-family: 'Poppins', sans-serif;
        font-size: 24px;
        width: 90%;

        @media (max-width: 1020px) {
            width: 94%;
        }

        @media (max-width: 700px) {
            width: 90%;
        }

        @media (max-width: 470px) {
            width: 85%;
        }
    }

    &__formInfo {
        display: flex;
        justify-content: space-between;
        margin-top: 32px;
        width: 45%;

        @media (max-width: 1070px) {
            width: 50%;
        }

        @media (max-width: 1020px) {
            width: auto;
        }

        @media (max-width: 700px) {
            flex-direction: column;
        }
    }

    &__formCourse {
        font-size: 14px;
        font-weight: 400;
        color: #585858;
        display: flex;
        flex-direction: column;
        gap: 6px;
    }

    &__formSubInfo {
        color: #868686;
        font-size: 14px;
        display: flex;
        flex-direction: column;
        gap: 6px;
    }

    &__formTime {
        display: flex;
        align-items: center;
        gap: 7px;
    }

    &__formReserve {
        display: flex;
        align-items: center;
        gap: 7px;

        @media (max-width: 700px) {
            justify-content: space-between;
        }

        button {
            border: none;
            background: transparent;
            color: #FE7F32;
            cursor: pointer;
        }
    }

    &__continue {
        margin-top: 26px;
        width: 45%;

        @media (max-width: 1020px) {
            width: auto;
        }

        button {
            background-color: #FE7F32;
            border: none;
            color: #fff;
            font-size: 16px;
            padding: 23px 0;
            border-radius: 16px;
            width: 100%;
            cursor: pointer;
        }
    }
}
</style>