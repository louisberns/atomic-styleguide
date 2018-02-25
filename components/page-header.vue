<template lang="html">
  <div class="page-header container">
    <div class="page-header__info">
      <titleHeader><span slot="title" class="page-header__title">{{ title }}</span></titleHeader>
      <span class="page-header__title sub-title">{{ subTitle }}</span>
      <p class="page-header__message">{{ message }}</p>
    </div>
  </div>
</template>

<script>
  import titleHeader from "@/components/titleHeader";

  export default {
    components: {
      titleHeader
    },
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
