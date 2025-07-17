<template>
  <CommonResponsiveContainer class="bg-white">
    <div class="resume px-3 justify-center lg:px-10 md:grid md:grid-cols-2 lg:py-10">
      <div class="resume__img flex justify-center mb-6 md:py-6">
        <div class="img__element outline outline-indigo-400 outline-offset-2"></div>
      </div>
      <div class="resume__body flex flex-col px-3 mb-6 justify-center md:mb-20 lg:justify-between py-10">
        <h2 class="text-2xl font-bold mb-2 md:text-3xl lg:3xl">Kevin Guzman</h2>
        <p class="text-gray-600 mb-6 md:text-lg lg:text-xl">
          <strong class="font-semibold text-emerald-400">Software Engineer</strong>, <strong class="font-semibold text-emerald-400">Back / Front Developer</strong>, with a lot of enthusiasm to continue helping to create software solutions for everyone. <strong class="font-semibold text-emerald-400">With my 10 years of experience in the tech environment</strong>, I have had the opportunity to learn, create, destroy and rebuild software of all kinds. How can I help you?
        </p>
        <div class="resume__body__controls flex justify-center">
          <CommonButtom class="body__controls__item bg-emerald-400" type="link" target="_blank">Download CV</CommonButtom>
        </div>
      </div>
      <div class="px-3 md:col-span-2 md:flex md:flex-wrap md:gap-8 md:justify-center xl:justify-between">
        <Skill v-for="(value, key) in skills" :id="key" :title="value.title" :items="value.items" :class="value.class"/>
      </div>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
const skills = {
  frontend: {
    title: 'Frontend',
    class: 'mb-5 md:w-80',
    items: [
      { name: 'VueJS', icon: 'vuedotjs.svg', level: 5 },
      { name: 'Lit E.', icon: 'lit.svg', level: 2 },
      { name: 'Angular', icon: 'angular.svg', level: 3 },
    ]
  },
  backend: {
    title: 'Backend',
    class: 'mb-5 md:w-80',
    items: [
      { name: 'Drupal', icon: 'drupal.svg', level: 4 },
      { name: 'Laravel', icon: 'laravel.svg', level: 4 },
      { name: 'Symfony', icon: 'symfony.svg', level: 3 },
      { name: 'Flask', icon: 'flask.svg', level: 2 },
    ]
  },
  other: {
    title: 'Other',
    class: 'mb-5 md:w-80',
    items: [
      { name: 'AWS', icon: 'amazonwebservices.svg', level: 3 },
      { name: 'MySQL', icon: 'mysql.svg', level: 4 },
      { name: 'Git / Github', icon: 'github.svg', level: 5 },
      { name: 'Docker', icon: 'docker.svg', level: 4 }
    ]
  }
};
</script>

<style>
  .img__element {
    background-image: url('public/profiles/profile.jpg');
    background-size: 13rem 13rem;
    height: 13rem;
    width: 13rem;
    border-radius: 80% 20% 32% 68% / 58% 22% 78% 42% ;
  }

  @media (width >= 48rem) {
    .img__element {
      background-size: 20rem 20rem;
      height: 20rem;
      width: 16rem;
    }
  }

  @media (width >= 80rem) {
    .img__element {
      background-size: 25rem 25rem;
      height: 20rem;
      width: 20rem;
    }
  }
</style>