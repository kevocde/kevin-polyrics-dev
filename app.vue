<script setup lang="ts">
let skills = {
  frontend: {
    title: 'Frontend',
    items: [
      { name: 'VueJS', icon: 'vuedotjs.svg' },
      { name: 'Lit E.', icon: 'lit.svg' },
      { name: 'Angular', icon: 'angular.svg' },
    ]
  },
  backend: {
    title: 'Backend',
    items: [
      { name: 'Drupal', icon: 'drupal.svg' },
      { name: 'Laravel', icon: 'laravel.svg' },
      { name: 'Symfony', icon: 'symfony.svg' },
      { name: 'Flask', icon: 'flask.svg' },
    ]
  },
  other: {
    title: 'Other',
    items: [
      { name: 'AWS', icon: 'amazonwebservices.svg' },
      { name: 'MySQL', icon: 'mysql.svg' },
      { name: 'Git / Github', icon: 'github.svg' },
      { name: 'Docker', icon: 'docker.svg' }
    ]
  }
};
</script>

<template>
  <div class="container mx-auto px-36">
    <Section id="main">
      <template v-slot:header>
        <h1 class="text-6xl mb-2">Hi, I'm Kevin G</h1>
        <h2 class="text-xl">Software Enginner | Software Developer</h2>
      </template>
      <template v-slot:body>
        <nav class="w-full text-center alt-nav">
          <ul class="flex gap-4 justify-center">
            <li class="cursor-pointer hover:underline"><a href="#skills">Skills</a></li>
            <li class="cursor-pointer hover:underline"><a href="#references">References</a></li>
            <li class="cursor-pointer hover:underline"><a href="#portfolio">Portfolio</a></li>
            <li class="cursor-pointer hover:underline"><a href="#contact">Contact</a></li>
          </ul>
        </nav>
      </template>
    </Section>
    <Section id="skills">
      <template v-slot:header>
        <h2 class="text-4xl text-center mb-2">Skills</h2>
        <h3 class="text-xl text-neutral-500">What Do I Use?</h3>
      </template>
      <template v-slot:body>
        <div class="flex mb-4 w-full px-20">
          <Skill v-for="(value, key) in skills" :id="key" :title="value.title" :items="value.items"/>
        </div>
      </template>
    </Section>
    <Section id="references">
      <template v-slot:header>
        <h2 class="text-4xl text-center mb-2">References</h2>
        <h3 class="text-xl text-neutral-500">Friends & Partners</h3>
      </template>
      <template v-slot:body>
      </template>
    </Section>
    <Section id="portfolio">
      <template v-slot:header>
        <h2 class="text-4xl text-center mb-2">Portfolio</h2>
        <h3 class="text-xl text-neutral-500">What Can I Do?</h3>
      </template>
      <template v-slot:body>
      </template>
    </Section>
    <Section id="contact">
      <template v-slot:header>
        <h2 class="text-4xl text-center mb-2">Contact</h2>
        <h3 class="text-xl text-neutral-500">Need a Hand?</h3>
      </template>
      <template v-slot:body>
      </template>
    </Section>
  </div>
</template>
