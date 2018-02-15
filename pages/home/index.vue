<template lang="html">
  <div id="home" class="container column">
    <pageIndex :title="info.index.banner.title">
      <img slot="image" src="@/static/logo.svg" />
    </pageIndex>
    <pageHeader :title="info.index.title" :subTitle="info.index.subTitle" :message="info.index.message" />
  </div>
</template>

<script>
import info from '@/static/data/info.json';
import pageIndex from '@/components/page-header-index';
import pageHeader from '@/components/page-header';

export default {
  name: 'home',
  components: {
    pageIndex,
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
