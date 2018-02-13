<template lang="html">
  <div id="style" class="">
    <pageHeader :title="info.style.title" :subTitle="info.style.subTitle" :message="info.style.message" />
    <sectionPrev :items="base.menuPane.routes[3].subRoute" />
  </div>
</template>

<script>
  import base from '@/static/data/base.json';
  import info from '@/static/data/info.json';
  import pageHeader from '@/components/page-header';
  import sectionPrev from '@/components/section-preview';

  export default {
    components: {
      pageHeader,
      sectionPrev
    },
    data() {
      return {
        base,
        info
      }
    }
  }
</script>

<style lang="css">
</style>
