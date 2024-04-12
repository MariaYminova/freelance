<template>
  <header>
    <div class="header">
      <div class="header__person">
        <div class="header__avatar"></div>
        <div>
          <div class="header__text">MARIA YMINOVA</div>
          <div class="header__description">frontend developer web designer</div>

          <div class="header__wrap-link">
            <a
              class="header__link"
              href="https://t.me/maria_yminova"
              target="_blank"
            >
              <img src="../assets/icons/icon-telegram.svg" alt="" />
            </a>

            <a
              class="header__link"
              href="https://github.com/MariaYminova"
              target="_blank"
            >
              <img src="../assets/icons/icon-gh.svg" alt="" />
            </a>

            <a
              class="header__link"
              href="https://www.fl.ru/users/vabylia96/portfolio/"
              target="_blank"
            >
              <img src="../assets/icons/icon-fl.svg" alt="" />
            </a>
          </div>
        </div>
      </div>
      <div class="header__info">
        <div class="header__skills">Адаптивная верстка</div>
        <div class="header__skills">Официальное сотрудничество</div>
        <div class="header__skills">Поддержка и сопровождение</div>
        <div class="header__skills">Pixel Perfect</div>
        <div class="header__skills">Git</div>
        <div class="header__skills">Java Script</div>

        <div class="header__skills">Vue.js</div>
        <div class="header__skills">SCSS (БЭМ)</div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "PageHeader",
};
</script>

<style lang="scss">
.header {
  margin-bottom: 70px;
  display: flex;

  @media (max-width: 955px) {
    display: block;
  }

  &__person {
    display: flex;
    align-items: center;
    margin-right: 119px;

    @media (max-width: 955px) {
      margin-bottom: 36px;
    }

    @media (max-width: 540px) {
      display: block;
    }
  }

  &__avatar {
    background-image: url("../assets/icons/img-avatar.png");
    height: 151px;
    width: 155px;
    margin-right: 24px;
    filter: drop-shadow(3px 2px 1px #0000000f);

    @media (max-width: 540px) {
      margin-bottom: 16px;
    }
  }

  &__text {
    font-size: 36px;
    margin-bottom: 8px;
    width: 160px;

    @media (max-width: 540px) {
      width: 285px;
    }
  }

  &__description {
    font-size: 18px;
    margin-bottom: 16px;
    width: 160px;
  }

  &__info {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
  }

  &__skills {
    margin: 0 0 20px 20px;
    padding: 15px 50px;
    background-color: #fff;
    border-radius: 50px;
    font-size: 18px;
    filter: drop-shadow(3px 2px 1px #0000000f);

    @media (max-width: 955px) {
      margin: 0 20px 20px 0;
    }

    @media (max-width: 540px) {
      padding: 10px 30px;
      font-size: 16px;
      margin: 0 12px 12px 0;
    }
  }

  &__wrap-link {
    display: flex;
    gap: 15px;
  }

  &__link {
    filter: drop-shadow(3px 2px 1px #0000000f);

    &:hover {
      filter: drop-shadow(2px 2px 1px #3d86ab81);
      transition: filter 0.2s, transform 1s;

      @media (max-width: 955px) {
        filter: none;
      }
    }
  }
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
