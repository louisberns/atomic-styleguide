<template lang="html">
  <!--menu pane content-->
  <div class="menu-pane container column">
    <ul class="menu-pane__list">
      <li class="menu-pane__item" v-for="item in base.menuPane.routes" v-if="!item.subRoute">
        <router-link :to="{ path: item.src }" class="menu-pane__item__link">{{ item.title }}</router-link>
      </li>
      <li class="menu-pane__item dropdown" v-else-if="item.subRoute">
          {{ item.title }}
          <!--<img src="" alt="Dropdown toggle arrow" v-if="item.subRoute">-->
          <ul class="menu-pane__sub-items__list">
            <li class="menu-pane__sub-item" v-for="subItem in item.subRoute">
              <router-link :to="{ path: subItem.src }" class="menu-pane__item__link">{{ subItem.title }}</router-link>
            </li>
          </ul>
      </li>
    </ul>
  </div>
</template>

<script>
import base from '@/static/data/base.json';

export default {
  data() {
    return {
      base
    }
  }
}
</script>

<style lang="scss">
</style>
