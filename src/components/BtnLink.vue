<template>
  <a :href="url" target="_blanc"> <button class="btn-link">Перейти</button></a>
</template>

<script>
export default {
  name: "BtnLink",

  props: {
    url: {
      type: String,
    },
  },
};
</script>

<style lang="scss">
.btn-link {
  width: 140px;
  padding: 10px 30px;
  background-color: #e2eeec;
  border-radius: 30px;
  font-size: 16px;

  @media (max-width: 580px) {
    font-size: 14px;
    margin-bottom: 12px;
    padding: 8px 30px;
  }

  &:hover {
    filter: drop-shadow(2px 2px 1px #3d86ab81);
    transition: filter 0.2s, transform 1s;

    @media (max-width: 955px) {
      filter: none;
    }
  }

  &:not(:hover) {
    filter: none;
    transition: filter 0.4s, transform 1s;
  }
}
</style>
