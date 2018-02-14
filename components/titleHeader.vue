<template>
<div>

  <div class="title padding-left-20 ">
    <h1><slot name="title"></slot></h1>
  </div>

</div>
</template>

<script>
export default {
  name: 'titleHeader',
  data() {
    return {

    }
  },
  props: {},
}
</script>

<style lang="scss" scoped>
.title {
    padding-bottom: 50px;
    h2 {
        position: relative;
        &::after {
            content: '';
            display: block;
            position: absolute;
            background: #ffff00;
            width: 10%;
            height: 30px;
            left: 0;
            bottom: 0;
            z-index: -2;
        }
    }
}
</style>
