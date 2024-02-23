<template>
  <div class="header">
    <div class="header__container">
      <div><img src="@/assets/svg/logo.svg" alt=""></div>
      <nav class="header__nav">
        <ul>
          <li>
            <a href="/">Как обменять?</a>
          </li>
          <li><a href="/">О нас</a></li>
          <li><a href="/">Отзывы</a></li>
          <li><a href="/">Партнерская программа</a></li>
        </ul>
      </nav>
      <button class="header__login">Вход и регистрация</button>
      <div class="header__mobButtons">
        <img src="@/assets/svg/user.svg" alt="">
        <img src="@/assets/svg/burger.svg" alt="">
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
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__nav {
    ul {
      display: flex;
      gap: 44px;
      font-size: 16px;

      li {
        list-style: none;
      }
    }

    a {
      text-decoration: none;
      color: var(--dark-grey);
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
    background-color: var(--light-grey);
  }
}
</style>
