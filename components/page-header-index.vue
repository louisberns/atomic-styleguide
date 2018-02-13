<template lang="html">
  <div class="page-header index-page container">
    <div class="page-header__info" v-if="info.index">
      <h1 class="page-header__title"> {{ info.index.title }} </h1>
      <span class="page-header__title sub-title"> {{ info.index.subTitle }} </span>

      <p class="page-header__message"> {{ info.index.message }} </p>

      <div class="page-header__image">
        <img src="" alt="">
      </div>
    </div>
    <aside class="page-header__aside container">

    </aside>
  </div>
</template>

<script>
import info from '@/static/data/info.json';

export default {
  data() {
    return {
      info
    }
  }
}
</script>

<style lang="css">
</style>
