<template>
  <template v-if="type === BUTTON_TYPE">
    <button v-bind="$attrs"><slot></slot></button>
  </template>
  <template v-else-if="type === LINK_TYPE">
    <a class="text-white rounded-full px-6 py-2 cursor-pointer" v-bind="$attrs"><slot></slot></a>
  </template>
</template>

<script lang="ts" setup>
  const BUTTON_TYPE = 'button';
  const LINK_TYPE = 'link';

  defineProps({
    type: {type: String, default: BUTTON_TYPE},
  })
</script>

<style>

</style>