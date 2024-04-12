<template>
  <div class="row">
    <div
      v-for="card in projectCards"
      class="col-xs-12 col-sm-12 col-md-6 col-lg-6"
    >
      <ProjectCard class="catalog-projects__card" :card="card" :key="card.id" />
    </div>
  </div>
</template>

<script>
import ProjectCard from "./ProjectCard.vue";

export default {
  name: "CatalogProject",

  components: {
    ProjectCard,
  },

  props: {
    projectCards: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.catalog-projects {
  &__wrap {
    display: flex;
    flex-wrap: wrap;
  }

  &__card {
    margin: 0 0 36px 0;
  }
}
</style>
