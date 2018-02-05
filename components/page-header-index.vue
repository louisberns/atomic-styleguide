<template lang="html">
  <div class="container">
    <div class="">
      <img src="" alt="">
    </div>
    <div class="">
      <h1>Hospitalar Styleguide</h1>
      <p>Referência de estilo e interações para front-end consistente e melhor experiência do usuário.</p>
    </div>
    <div class="" v-if="info.index">
      <h1> {{ info.index.title }} </h1>
      <p> {{ info.index.message }} </p>
    </div>
  </div>
</template>

<script>
import info from '@/static/data/base.json';

export default {
  data() {
    return {
      info
    }
  }
}
</script>

<style lang="css">
</style>
