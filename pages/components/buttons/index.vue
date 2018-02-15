<template lang="html">
  <div id="buttons" class="">
    <pageHeader :title="info.components.items.buttons.title" :subTitle="info.components.items.buttons.subTitle" :message="info.components.items.buttons.message" />
    <codeMirror/>
    <componentInfo :title="info.components.items.buttons.titleInfo" :message="info.components.items.buttons.infoMessage" :listItem="info.components.items.buttons.listInfo"/>
  </div>
</template>

<script>
  import info from '@/static/data/info.json';
  import base from '@/static/data/base.json';
  import pageHeader from '@/components/page-header';
  import codeMirror from '@/components/code-mirror';
  import componentInfo from '@/components/component-info';

  export default {
    components: {
      pageHeader,
      codeMirror,
      componentInfo
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
