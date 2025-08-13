<template>
  <CommonResponsiveContainer class="resume">
    <div class="grid grid-col-1 md:grid-cols-2">
      <div class="profile__cover px-4 py-8 flex justify-center md:py-12">
        <div class="conver__img overflow-hidden rounded-2xl outline outline-emerald-500 outline-offset-2 w-48 md:w-64 lg:w-80">
          <img src="public/profiles/profile.jpg" alt="">
        </div>
      </div>
      <div class="profile__resume px-4 md:flex md:flex-col md:justify-center mb-8">
        <h2 class="font-bold text-2xl mb-4 lg:text-3xl">Kevin Guzman</h2>
        <p class="text-gray-500 text-md mb-4 lg:text-lg">
          <strong class="font-semibold text-emerald-400">Software Engineer</strong>, <strong class="font-semibold text-emerald-400">Back / Front Developer</strong>, with a lot of enthusiasm to continue helping to create software solutions for everyone. <strong class="font-semibold text-emerald-400">With my 10 years of experience in the tech environment</strong>, I have had the opportunity to learn, create, destroy and rebuild software of all kinds. How can I help you?
        </p>
        <div class="flex">
          <CommonButtom class="bg-emerald-400 hover:bg-emerald-500 hover:animation-shake" type="link" target="_blank">Download CV</CommonButtom>
        </div>
      </div>
      <div class="profile__skills px-4 md:col-span-2 md:flex md:flex-wrap md:gap-x-8 md:justify-center xl:gap-x-12 xl:py-12">
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

<style lang="scss">
  .resume {
    padding-top: 10rem;
    padding-bottom: 10rem;

    .profile__cover {
      .conver__img {
        transform: rotate(-2deg);
      }
    }
  }
</style>