<template lang="html">
  <div class="page-header container column">
    <h1 class="page-header__title">{{ title }}</h1>
    <p class="page-header__message">{{ message }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
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
