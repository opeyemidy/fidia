<template>
  <nuxt-link :to="to" :class="['nav-link', { 'link-submenu': submenu }]">
    <span class="link-icon">
      <slot name="icon"></slot>
    </span>
    <span class="link-title"><slot></slot></span>
  </nuxt-link>
</template>
<script>
export default {
  props: {
    to: {
      type: String,
      default: () => '',
    },
    name: {
      type: String,
      default: () => '',
    },
    nuxt: {
      type: Boolean,
      default: () => false,
    },
    dropDown: {
      type: Boolean,
      default: () => false,
    },
    submenu: {
      type: Boolean,
      default: () => false,
    },
  },
}
</script>
