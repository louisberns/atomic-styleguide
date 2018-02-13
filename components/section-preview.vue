<template lang="html">
  <div class="section-prev container">
    <div class="section-prev__item" v-for="item in items">
      <router-link :to="{ path: item.src }">
        <h3 class="item__title">{{ item.title }}</h3>
        <p class="item__text">{{ item.text }}</p>
      </router-link>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      items: {
        type: Array
      }
    }
  }
</script>

<style lang="scss" scoped>
  .section-prev {
    flex-wrap: wrap;

    .section-prev__item {
      border: 1px solid #000;
      min-width: 270px;
      min-height: 125px;
      margin: 10px;
      box-sizing: border-box;
      padding: 5px 10px;

      a {
        width: 100%;
        height: 100%;
      }
    }
  }

</style>
