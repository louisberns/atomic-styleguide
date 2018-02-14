<template lang="html">
  <div id="home" class="container size margin">
    <pageIndex/>
    <pageHeader :title="info.index.title" :subTitle="info.index.subTitle" :message="info.index.message" />
  </div>
</template>

<script>
import info from '@/static/data/info.json';
import pageIndex from '@/components/page-header-index';
import pageHeader from '@/components/page-header';

export default {
  components: {
    pageIndex,
    pageHeader
  },
  data() {
    return {
      info,
      title: 'Atomic Design System',
      message: 'A set of components and style guides bounded with our principles.'
    }
  }

}
</script>

<style lang="css">
</style>
