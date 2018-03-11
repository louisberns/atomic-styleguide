<template lang="html">
  <!--menu pane content-->
  <div class="menu-box">
    <div class="menu-pane container column">
      <div class="menu-pane__logo">
        <router-link :to="{ path: base.menuPane.routes[0].src }">
          <img src="@/static/logo.svg" alt="Menu logo for Design System Template">
        </router-link>
      </div>
      <ul class="menu-pane__list">
        <li class="menu-pane__item" v-for="item in base.menuPane.routes" v-if="!item.subRoute">
          <router-link :to="{ path: item.src }" class="menu-pane__item__link">{{ item.title }}</router-link>
        </li>
        <li class="menu-pane__item dropdown" v-else-if="item.subRoute">
            <!--<router-link :to="{ path: item.src }" class="menu-pane__item__link">{{ item.title }}</router-link>-->
            <div class="menu-pane__item__link justify-content-between" v-on:click="toggleMenu(), clickToggle = !clickToggle">
              <router-link :to="{ path: item.src }" class="menu-pane__item__link">
                <span>{{ item.title }}</span>
                <span class="dropdown__icon dropdown__trigger margin-right-30"><i class="fas fa-chevron-right"></i></span>
              </router-link>
            </div>
            <div class="dropdown__list-container" v-if="clickToggle">
              <ul class="menu-pane__sub-items__list dropdown__list">
                <li class="menu-pane__sub-item" v-for="subItem in item.subRoute">
                  <router-link :to="{ path: subItem.src }" class="menu-pane__item__link">{{ subItem.title }}</router-link>
                </li>
              </ul>
            </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import base from '@/static/data/base.json';

export default {
  data() {
    return {
      base,
      clickToggle: true
    }
  }
}
</script>

<style lang="scss">
.dropdown__icon {
  position: absolute;
  right: 10px;
  z-index: 100;

  .fa-chevron-right {
    &.closed {
      transform: rotate(90deg);
    }
  }
}
.dropdown__trigger {
  cursor: pointer;
}
.dropdown__list-container {
  transition: 1s;
}
</style>
