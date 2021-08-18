<template>
  <div class="link-menu">
    <button class="nav-link active link-submenu">
      <span class="link-icon">
        <slot name="icon"></slot>
      </span>
      <span class="link-title"> {{ name }}</span>
    </button>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: () => '',
    },
  },
}
</script>
