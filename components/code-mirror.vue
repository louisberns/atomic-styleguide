<template lang="html">
  <div class="code-mirror margin-5pc">
    <pre>
      <code class="code-block html">{{ codeExample }}</code>
      <slot name="codeSlot" class="code-block"></slot>

    </pre>
  </div>
</template>

<script>

  export default {
    props: {
      codeExample: {
        type: String
      }
    }
  }
</script>

<style lang="scss" scoped>
  .code-block {
    border-radius: 5px;
    padding: 15px;
    box-sizing: border-box;
  }

</style>
