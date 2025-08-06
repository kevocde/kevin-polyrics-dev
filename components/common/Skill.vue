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
});

const range = (from: any, until: any) => {
  return [...Array(until-from).keys()].map(i => i + from)
}
</script>

<template>
  <div>
    <h3 class="text-lg font-semibold mb-4 lg:text-xl">{{ title }}</h3>
    <ul class="flex flex-col gap-4">
      <li v-for="item in items"  class="flex justify-between">
        <div class="flex items-center">
          <i class="mr-4">
            <img :src="`/icons/${item.icon}`" class="w-6 accent-color"></img>
          </i>
          <span class="text-gray-500 lg:text-lg">{{ item.name }}</span>
        </div>
        <div class="indicator flex gap-1 py-2">
          <div class="element w-5 h-full" v-for="level in range(1, 6)" :class="{'bg-emerald-500': (level <= item.level), 'bg-emerald-100': (level > item.level)}"></div>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped>
  .accent-color {
    filter: invert(49%) sepia(7%) saturate(782%) hue-rotate(182deg) brightness(89%) contrast(99%);
  }
</style>
