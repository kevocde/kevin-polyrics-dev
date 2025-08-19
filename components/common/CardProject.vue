<template>
  <div class="card-project bg-indigo-50 rounded-xl overflow-hidden">
    <div class="card-project__body h-48 lg:h-64 xl:h-80 overflow-hidden">
      <div v-if="description.trim().length > 0" class="body__description">
        <div class="description__bg" :style="['background-image: url(\'' + coverImg + '\')']"></div>
        <p class="description__text p-4 text-indigo-500 text-md lg:text-lg" :class="{'text-white': (coverImg.length > 0)}" v-html="description"></p>
      </div>
      <div v-else class="body__description p-4">
        <div class="space-y-4 mb-4">
          <div class="grid grid-cols-3 gap-4">
            <div class="col-span-2 h-3 rounded bg-indigo-400"></div>
            <div class="h-3 rounded bg-indigo-400"></div>
          </div>
          <div class="h-3 rounded bg-indigo-400"></div>
        </div>
        <div class="h-3 rounded bg-indigo-400"></div>
      </div>
    </div>
    <div class="card-project__footer p-4 flex bg-indigo-400 text-white">
      <div class="footer__title flex-1 text-lg"><span>{{ title }}</span></div>
      <div class="footer__actions flex gap-2 align-center">
        <a target="_blank" :href="github" class="actions__element"><img :src="`/icons/github.svg`" class="w-6 accent-color"></a>
        <a target="_blank" :href="website" class="actions__element text-2xl"><i class="lni lni-link-2-angular-right"></i></a>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
  defineProps({
    title: { type: String, default: 'Card title' },
    description: { type: String, default: '' },
    coverImg: { type: String, default: '' },
    github: { type: String, default: '' },
    website: { type: String, default: '' }
  })
</script>

<style>
  .card-project__body {
    position: relative;
  }

  .description__bg {
    position: absolute;
    top: 0;
    width: 100%;
    height: fill-available;
    filter: blur(5px);
  }

  .description__text {
    position: relative;
  }

  .accent-color {
    filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(351deg) brightness(109%) contrast(103%);
  }
</style>