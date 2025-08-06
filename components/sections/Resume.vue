<template>
  <CommonResponsiveContainer class="bg-white resume-ct">
    <div class="resume justify-center px-4 md:grid md:grid-col-2 md:gap-8">
      <div class="resume__img mb-8">
        <div class="img__element outline outline-indigo-400 outline-offset-2"></div>
      </div>
      <div class="resume__body flex flex-col mb-8 lg:flex lg:flex-col lg:justify-center ">
        <h2 class="text-2xl font-bold mb-4 md:text-3xl lg:3xl">Kevin Guzman</h2>
        <p class="text-gray-600 mb-4 md:text-lg lg:text-xl">
          <strong class="font-semibold text-emerald-400">Software Engineer</strong>, <strong class="font-semibold text-emerald-400">Back / Front Developer</strong>, with a lot of enthusiasm to continue helping to create software solutions for everyone. <strong class="font-semibold text-emerald-400">With my 10 years of experience in the tech environment</strong>, I have had the opportunity to learn, create, destroy and rebuild software of all kinds. How can I help you?
        </p>
        <div class="resume__body__controls flex justify-center">
          <CommonButtom class="body__controls__item bg-emerald-400" type="link" target="_blank">Download CV</CommonButtom>
        </div>
      </div>
      <div class="px-3 md:col-span-2 md:flex md:flex-wrap md:justify-center md:gap-8 lg:gap-12">
        <CommonSkill v-for="(value, key) in skills" :id="key" :title="value.title" :items="value.items" :class="value.class"/>
      </div>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
import { CommonSkill } from '#components';

const skills = {
  frontend: {
    title: 'Frontend',
    class: 'mb-6 md:w-80',
    items: [
      { name: 'VueJS', icon: 'vuedotjs.svg', level: 5 },
      { name: 'Lit E.', icon: 'lit.svg', level: 2 },
      { name: 'Angular', icon: 'angular.svg', level: 3 },
    ]
  },
  backend: {
    title: 'Backend',
    class: 'mb-6 md:w-80',
    items: [
      { name: 'Drupal', icon: 'drupal.svg', level: 4 },
      { name: 'Laravel', icon: 'laravel.svg', level: 4 },
      { name: 'Symfony', icon: 'symfony.svg', level: 3 },
      { name: 'Flask', icon: 'flask.svg', level: 2 },
    ]
  },
  other: {
    title: 'Other',
    class: 'mb-6 md:w-80',
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
  .resume-ct {
    height: 90rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .resume__img {
    display: flex;
    justify-content: center;
  }

  .resume__img .img__element {
    background-image: url('public/profiles/profile.jpg');
    background-size: 75vw;
    height: 75vw;
    width: 75vw;
    border-radius: 80% 20% 32% 68% / 58% 22% 78% 42% ;
  }

  @media (width >= 48rem) {
    .resume-ct {
      height: 65rem;
    }

    .resume__img .img__element {
      background-size: 45vw;
      height: 45vw;
      width: 45vw;
    }
  }

  @media (width >= 64rem) {
    .resume-ct {
      height: 75rem;
    }

    .resume__body {
      width: 40vw;
      max-width: 40rem;
    }

    .resume__img .img__element {
      background-size: 27.5rem;
      height: 27.5rem;
      width: 27.5rem;
    }
  }
</style>