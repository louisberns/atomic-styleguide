<template lang="html">
  <div class="container">
    <pageHeader :title="title" :message="message" />
  </div>
</template>

<script>
import pageHeader from '@/components/page-header';

export default {
  components: {
    pageHeader
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
