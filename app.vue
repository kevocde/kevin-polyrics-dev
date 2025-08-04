<template>
  <SectionsMainNav></SectionsMainNav>
  <SectionsProfile id="profile"></SectionsProfile>
  <SectionsResume id="resume"></SectionsResume>
  <SectionsWorkingOn id="workingon"></SectionsWorkingOn>
    <div class="container mx-auto px-36">
    <Section id="contact">
      <template v-slot:header>
        <h2 class="text-4xl text-center mb-2">Contact</h2>
        <h3 class="text-xl text-neutral-500">Need a Hand?</h3>
      </template>
      <template v-slot:body>
        <ContactList :links="links"/>
      </template>
    </Section>
  </div>
</template>
<script setup lang="ts">

const skills = {
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

const references = [
  {
    name: 'Mauricio Galindo',
    review: 'Id eum dignissimos sint earum odio eaque, et necessitatibus ullam recusandae quos facere rem quasi, quis optio. Obcaecati sed possimus adipisci sapiente.',
    position: 'Lider Técnico',
    company: 'Millicom',
    inclination: 'right'
  },
  {
    name: 'Mauricio Galindo',
    review: 'Id eum dignissimos sint earum odio eaque, et necessitatibus ullam recusandae quos facere rem quasi, quis optio. Obcaecati sed possimus adipisci sapiente.',
    position: 'Lider Técnico',
    company: 'Millicom',
    inclination: 'left',
  }
];

const links = [
  {
    label: 'GitHub',
    url: 'https://github.com/polyrico',
    icon: 'github.svg'
  },
  {
    label: 'E-Mail',
    url: 'mailto:kevind.guzmand@gmail.com',
    icon: 'maildotru.svg'
  },
  {
    label: 'LinkedIn',
    url: 'https://www.linkedin.com/in/kevocde',
    icon: 'linkedin.svg'
  }
];

const sections = [
  'main', 'skills', 'references', 'portfolio', 'contact',
];

</script>