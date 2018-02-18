<template lang="html">
  <div class="code-mirror">
    <pre>
      <code class="hljs">
        {{ codeExample }}
      </code>
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

<style lang="scss">
</style>
