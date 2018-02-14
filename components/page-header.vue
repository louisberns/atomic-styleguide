<template lang="html">
  <div class="page-header container">
    <div class="page-header__info">
      <h1 class="page-header__title">{{ title }}</h1>
      <span class="page-header__title sub-title">{{ subTitle }}</span>
      <p class="page-header__message">{{ message }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    },
    subTitle: {
      type: String
    },
    message: {
      type: String
    }
  }
}
</script>

<style lang="css">
</style>
