<template lang="html">
  <div class="card-item">
    <router-link :to="{ path: src }" class="item__link">
      <h3 class="item__title">{{ title }}</h3>
      <p class="item__text">{{ text }}</p>
    </router-link>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String
    },
    title: {
      type: String
    },
    text: {
      type: String
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '../assets/css/base/variables.scss';

  .card-item {
    border: 1px solid #000;
    min-width: 270px;
    min-height: 125px;
    margin: 10px;
    box-sizing: border-box;
    padding: 5px 10px;

    .item__link {
      width: 100%;
      height: 100%;
      color: $color-gray-dark;

      &:hover {
        color: $color-black;
      }
    }
  }
</style>
