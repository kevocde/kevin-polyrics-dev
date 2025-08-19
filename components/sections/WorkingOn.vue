<template>
  <CommonResponsiveContainer class="workingon">
    <div class="workingon__title px-4 text-center font-bold mb-10">
      <h3 class="text-2xl md:text-3xl xl:text-4xl">Working On</h3>
      <p class="text-gray-500 text-sm md:text-md xl:text-lg">Projects, Contributions, Ideas and more</p>
    </div>
    <div class="workingon__projects px-4 grid gap-4 md:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-4">
      <CommonCardProject v-for="project in projects" :title="project.title" :description="project.description" :coverImg="project.coverImg" :github="project.github" :website="project.website"></CommonCardProject>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
  const projects = [
    {
      title: 'Polyrics Labs',
      description: 'Sitio Web de Polyrics Labs, iniciativa de laboratorio de desarrollo de código <strong>Open-Source</strong>, <strong>Minimalista</strong> y <strong>Funcional</strong>.',
      coverImg: 'https://t2.genius.com/unsafe/344x344/https%3A%2F%2Fimages.genius.com%2Fb7aef36663862fcbb0ad08b9e3bf05a3.640x640x1.jpg',
      github: 'https://github.com/polyrico/Polyrics-Labs',
      website: 'https://polyrics.dev',
    },
    {
      title: 'Foundify',
      description: 'Plataforma tipo marketplace para publicar objetos perdidos.',
      github: 'https://github.com/orgs/Polyrics-Labs/repositories',
      website: 'https://foundify.polyrics.dev',
    },
    {
      title: 'My Home Cloud',
      description: 'Mi nube privada, al alcance de todos, PiHole, Plex, Servicios para desarrollo, VPN y más.',
    },
    {
      title: 'CloudShare',
      description: 'Espacio en la nube infinito, uniendo todas las APIs de servicios Cloud para expandir el espacio en la nube.',
    },
  ];
</script>

<style>
  .workingon {
    padding-top: 10rem;
    padding-bottom: 10rem;
  }
</style>