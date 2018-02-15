<template lang="html">
  <div class="section-prev container">
    <div class="section-prev__item" v-for="item in items">
      <cardPreview :src="item.src" :title="item.title" :text="item.text" />
    </div>
  </div>
</template>

<script>
  import cardPreview from '@/components/card-preview';

  export default {
    components: {
      cardPreview
    },
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
    }
  }

</style>
