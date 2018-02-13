<template lang="html">
  <div id="components" class="">
    <pageHeader :title="info.components.title" :subTitle="info.components.subTitle" :message="info.components.message" />
    <sectionPrev :items="base.menuPane.routes[2].subRoute" />
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
