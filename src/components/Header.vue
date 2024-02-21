<template>
  <div class="header">
    <div class="header__container">
      <div><img src="../assets/svg/logo.svg" alt=""></div>
      <div class="header__nav">
        <a href="/">Как обменять?</a>
        <a href="/">О нас</a>
        <a href="/">Отзывы</a>
        <a href="/">Партнерская программа</a>
      </div>
      <button class="header__login">Вход и регистрация</button>
      <div class="header__mobButtons">
        <img src="../assets/svg/user.svg" alt="">
        <img src="../assets/svg/burger.svg" alt="">
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  background-color: #FFFFFF94;

  &__container {
    max-width: 1180px;
    margin: 0 auto;
    padding: 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__nav {
    display: flex;
    gap: 44px;
    font-size: 16px;

    a {
      text-decoration: none;
      color: #585858;
    }

    @media (max-width: 1130px) {
      gap: 10px;
    }

    @media (max-width: 1020px) {
      display: none;
    }
  }

  &__login {
    color: #FE7F32;
    background-color: transparent;
    font-size: 16px;
    border: 1px solid #FE7F32;
    border-radius: 12px;
    padding: 13px 24px;
    cursor: pointer;

    @media (max-width: 1020px) {
      display: none;
    }
  }

  &__mobButtons {
    display: none;

    img {
      cursor: pointer;
    }

    @media (max-width: 1020px) {
      display: flex;
      gap: 30px;
    }
  }

  @media (max-width: 1020px) {
    background-color: #f9f8f8;
  }
}
</style>
