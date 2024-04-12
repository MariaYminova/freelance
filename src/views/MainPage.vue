<template>
  <main>
    <div class="projects-heading">Последние проекты</div>
    <CatalogProject :projectCards="projectCards" />
  </main>
</template>

<script>
import ProjectCard from "../components/ProjectCard.vue";
import CatalogProject from "../components/CatalogProject.vue";

export default {
  name: "MainPage",

  components: {
    ProjectCard,
    CatalogProject,
  },

  data() {
    return {
      projectCards: [
        {
          id: 1,
          title: "Oishi Sushi",
          description: "Сервис доставки японской кухни",
          img: "src/assets/icons/img-oishi-sushi.jpg",
          url: "https://mariayminova.github.io/oishi-susi/",
        },
        {
          id: 2,
          title: "Viewing Cats",
          description: "Католог просмотра пород кошек",
          img: "src/assets/icons/img-cats.jpg",
          url: "https://mariayminova.github.io/viewing-cats/",
        },
        {
          id: 3,
          title: "Birds and Bees",
          description: "Информационный сайт ресторанного бизнеса",
          img: "src/assets/icons/img-restaurant.jpg",
          url: "https://mariayminova.github.io/birds-and-bees/",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.projects-heading {
  font-size: 56px;
  margin-bottom: 52px;

  @media (max-width: 580px) {
    font-size: 36px;
    margin-bottom: 36px;
  }
}
</style>
