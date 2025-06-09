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
        <Reference v-for="(value, key) in references" :name="value.name" :review="value.review" :position="value.position" :company="value.company" :inclination="value.inclination"/>
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
        <ContactList :links="links"/>
      </template>
    </Section>
  </div>
</template>
