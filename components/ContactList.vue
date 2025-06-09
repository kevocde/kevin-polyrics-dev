<script setup lang="ts">
const props = defineProps({
  links: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <ul class="flex gap-4 justify-center">
    <li v-for="link in links" class="cursor-pointer hover:underline">
      <a :href="link.url" class="block px-4 py-3 min-w-30 flex hover:outline-1" target="_blank">
        <i class="mr-2">
          <img :src="`icons/${link.icon}`" class="w-6">
        </i>
        <span>{{ link.label }}</span>
      </a>
    </li>
  </ul>
</template>