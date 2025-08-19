<template>
  <CommonResponsiveContainer class="experiencie">
    <div class="experiencie__title px-4 text-center font-bold mb-10">
      <h3 class="text-2xl md:text-3xl xl:text-4xl">Work Experiencie</h3>
      <p class="text-gray-500 text-sm md:text-md xl:text-lg">My trajectory in this +8 years</p>
    </div>
    <div class="experiencie__timeline px-4 flex justify-center">
      <ol class="timeline">
        <li v-for="experience in experiencies" class="timeline__item border-l-4 border-emerald-500">
          <div class="item__wrap flex flex-start">
            <div class="wrap__icon w-8 h-8 text-lg flex items-center justify-center rounded-full bg-emerald-500 text-emerald-50 -ml-3.5 md:-ml-4.5 md:text-xl">
              <i class="lni lni-calendar-days invisible md:visible"></i>
            </div>
            <div class="wrap__body block bg-gray-100 rounded-xl p-6 ml-2 mb-5 cursor-pointer hover:bg-emerald-100 md:mb-10 md:ml-6">
              <div class="card__title text-gray-800 grid grid-cols-2 mb-4">
                <h3 class="text-lg mr-8 font-semibold">{{ experience.company }}</h3>
                <span class="text-md self-end text-end">{{ experience.time }}</span>
                <span class="cols-span-2 text-sm">{{ experience.position }}</span>
              </div>
              <div class="card__body text-gray-800">
                <p>{{ experience.description }}</p>
              </div>
            </div>
          </div>
        </li>
      </ol>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
  import type { ExperienceDto } from '~/typos/ExperienceDto';

  defineProps({
    experiencies: { type: Array<ExperienceDto>, required: true }
  });
</script>

<style>
  .experiencie {
    padding-top: 10rem;
    padding-bottom: 10rem;
  }

  .\-ml\-3\.5 {
    margin-left: -0.70rem;
  }

  .\-ml\-4\.5 {
    margin-left: -1.15rem;
  }

  @media (width >= 48rem) {
    .md\:\-ml\-4\.5 {
      margin-left: -1.15rem;
    }
  }
</style>