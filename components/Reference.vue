<script setup lang="ts">
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  review: {
    type: String,
    required: true
  },
  position: {
    type: String,
    required: true
  },
  company: {
    type: String,
    required: true
  },
  inclination: {
    type: String,
    required: true,
    default: 'left'
  }
});

const occupation = computed(() => {
  return `${props.position} | ${props.company}`
});

const profileImage = computed(() => {
  return `profiles/${props.name.replace(' ', '-').toLowerCase()}.png`
});

const toLeft = computed(() => {
  return props.inclination === 'left';
});

const toRight = computed(() => {
  return props.inclination === 'right';
});
</script>

<template>
  <div class="flex">
    <div class="flex flex-nowrap rounded-md p-4">
        <div v-if="toLeft" class="image flex justify-center rounded-full min-w-30 overflow-hidden mr-4 outline-3"><img class="aspect-3/2 object-cover" :src="profileImage" alt=""></div>
        <div class="flex flex-col justify-center">
            <p class="mb-4 italic">"{{ review }}"</p>
            <h3 class="font-semibold leading-none">{{ name }}</h3>
            <span class="text-sm text-neutral-500">{{ occupation }}</span>
        </div>
        <div v-if="toRight" class="image flex justify-center rounded-full min-w-30 overflow-hidden ml-4 outline-3"><img class="aspect-3/2 object-cover" :src="profileImage" alt=""></div>
    </div>
  </div>
</template>