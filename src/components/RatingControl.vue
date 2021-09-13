<template>
  <ul>
    <li :class="{ selected: modelValue === 'the' }" @click="active('the')">
      <button type="button">the</button>
    </li>
    <li :class="{ selected: modelValue === 'what' }" @click="active('what')">
      <button type="button">what</button>
    </li>
    <li :class="{ selected: modelValue === 'duck' }" @click="active('duck')">
      <button type="button">duck</button>
    </li>
  </ul>
</template>

<script>
export default {
  props: ['modelValue'],
  emits: ['update:modelValue'],
  methods: {
    active(option) {
      this.$emit('update:modelValue', option);
    }
  }
};
</script>

<style scoped>
li.selected {
  background: red;
}
</style>
