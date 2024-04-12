<template>
  <div class="container">
    <PageHeader />
    <MainPage />
  </div>
</template>

<script>
import MainPage from "./views/MainPage.vue";
import PageHeader from "./components/PageHeader.vue";

export default {
  components: {
    MainPage,
    PageHeader,
  },
};
</script>

<style>
.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
