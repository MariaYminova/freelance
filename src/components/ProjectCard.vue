<template>
  <div class="project-card">
    <div class="project-card__wrap">
      <div>
        <div class="project-card__title">{{ card.title }}</div>
        <p class="project-card__discription">
          {{ card.description }}
        </p>
      </div>
      <BtnLink :url="card.url" :key="card.id" />
    </div>
    <img class="project-card__img" :src="card.img" alt="" />
  </div>
</template>

<script>
import BtnLink from "./BtnLink.vue";

export default {
  name: "ProjectCard",

  components: {
    BtnLink,
  },

  props: {
    card: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.project-card {
  background-color: #fff;
  width: 100%;
  padding: 28px;
  border-radius: 5px;
  filter: drop-shadow(3px 2px 1px #0000000f);

  &__wrap {
    display: flex;
    justify-content: space-between;

    @media (max-width: 580px) {
      display: block;
    }
  }

  &__img {
    width: 100%;
    object-fit: contain;
    border-radius: 5px;
  }

  &__title {
    font-size: 32px;
    margin-bottom: 12px;
    max-width: 326px;
    height: 34px;
    overflow: hidden;

    @media (max-width: 580px) {
      font-size: 28px;
      margin-bottom: 4px;
    }
  }

  &__discription {
    font-size: 16px;
    margin-bottom: 24px;
    max-width: 326px;
    max-height: 33px;
    overflow: hidden;

    @media (max-width: 580px) {
      margin-bottom: 16px;
    }
  }
}
</style>
