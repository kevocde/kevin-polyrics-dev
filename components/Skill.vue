<script setup lang="ts">
defineProps({
  title: {
    type: String,
    required: true
  },
  items: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <div class="flex-1 p-4">
    <h3 class="text-lg mb-4 font-semibold text-center">{{ title }}</h3>
    <ul class="flex flex-col gap-4 items-center">
      <li v-for="item in items"  class="flex items-center">
        <i class="mr-4">
          <img :src="`icons/${item.icon}`" class="w-6"></img>
        </i>
        <span>{{ item.name }}</span>
      </li>
    </ul>
  </div>
</template>