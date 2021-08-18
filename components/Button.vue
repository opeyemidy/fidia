<template>
  <button
    :class="[
      'button',
      { 'tab-button': tab, 'btn-colored': colored, 'btn-disabled': disabled },
    ]"
    :disabled="disabled"
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
    disabled: {
      type: Boolean,
      default: false,
    },
    type: {
      type: String,
      default: () => 'button',
    },
  },
}
</script>
