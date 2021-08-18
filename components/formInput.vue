<template>
  <div class="input-container">
    <div class="input-title">
      <label :for="labelFor" class="input-label">{{ title }}</label>
      <slot name="link"></slot>
    </div>
    <div class="input-wrapper">
      <input v-model="inputValue" :type="type" :name="name" />
      <slot v-if="inputValue !== '' && type === 'password'" name="icon"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: '',
    },
    name: {
      type: String,
      default: 'text',
    },
    type: {
      type: String,
      default: 'text',
    },
    labelFor: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      inputValue: '',
    }
  },
}
</script>
