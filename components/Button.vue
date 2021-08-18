<template>
  <button
    :class="[
      'button',
      { 'tab-button': tab, 'btn-colored': colored, 'text-danger': false },
    ]"
    type="button"
    @click="$emit('click')"
  >
    <div class="btn-content">
      <span v-if="hasIcon" class="btn-icon">
        <slot name="icon"></slot>
      </span>
      <slot> </slot>
    </div>
  </button>
</template>

<script>
export default {
  props: {
    tab: {
      type: Boolean,
      default: false,
    },
    hasIcon: {
      type: Boolean,
      default: false,
    },
    colored: {
      type: Boolean,
      default: false,
    },
  },
}
</script>
