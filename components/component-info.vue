<template lang="html">
  <div class="content__info margin-5pc">
    <div class="" v-if="!message">
      <h3 class="title">{{ title }}</h3>
      <ul>
        <li v-for="i in listItem">{{ i.item }}</li>
      </ul>
    </div>
    <div class="" v-else-if="message && !listItem">
      <h3 class="title">{{ title }}</h3>
      <p v-if="message">{{ message }}</p>
    </div>
    <div class="" v-else-if="message && listItem">
      <h3 class="title">{{ title }}</h3>
      <p v-if="message">{{ message }}</p>
      <ul>
        <li v-for="i in listItem">{{ i.item }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      title: {
        type: String
      },
      message: {
        type: String
      },
      listItem: {
        type: Array
      }
    }
  }
</script>

<style lang="css">
</style>
