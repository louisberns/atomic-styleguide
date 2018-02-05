<template lang="html">
  <div id="home" class="container size margin">
    <pageIndex/>
  </div>
</template>

<script>
import pageIndex from '@/components/page-header-index';

export default {
  components: {
    pageIndex
  },
  data() {
    return {
      title: 'Atomic Design System',
      message: 'A set of components and style guides bounded with our principles.'
    }
  }

}
</script>

<style lang="css">
</style>
