<template lang="html">
  <div class="container about">
    <pageHeader :title="info.about.title" :subTitle="info.about.subTitle" :message="info.about.message" />
  </div>
</template>

<script>
  import pageHeader from '@/components/page-header';
  import info from '@/static/data/info.json';

  export default {
    components: {
      pageHeader
    },
    data() {
      return {
        info
      }
    }
  }
</script>

<style lang="css">
</style>
