<template lang="html">
  <div class="code-mirror margin-5pc">
    <pre>
      <!--<code class="hljs">
        <span v-for="i in codeExample">{{ i }}</span>
      </code>-->
      <slot name="codeSlot" class="hljs"></slot>
    </pre>
  </div>
</template>

<script>

  export default {
    props: {
      codeExample: {
        type: Array
      }
    }
  }
</script>

<style lang="scss">
</style>
