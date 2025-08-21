<template>
  <SectionsMainNav></SectionsMainNav>
  <SectionsProfile id="profile"></SectionsProfile>
  <SectionsResume id="resume"></SectionsResume>
  <SectionsWorkingOn id="workingon" :projects="projects"></SectionsWorkingOn>
  <SectionsExperiencie id="workexperience" :experiencies="experienices"></SectionsExperiencie>
  <SectionsContact id="contact"></SectionsContact>
  <SectionsFooter id="footer"></SectionsFooter>
</template>

<script setup>
  useSeoMeta({
    title: 'Kevin Guzman - Software Engineer, Back / Front Developer',
    ogTitle: 'Kevin Guzman - Software Engineer, Back / Front Developer',
    description: 'With my 10 years of experience in the tech environment, I have had the opportunity to learn, create, destroy and rebuild software of all kinds. How can I help you?',
    ogDescription: 'With my 10 years of experience in the tech environment, I have had the opportunity to learn, create, destroy and rebuild software of all kinds. How can I help you?',
    ogImage: '/profiles/profile.jpg',
    ogUrl: 'https://kevin.polyrics.dev',
    ogType: 'website',
    keywords: 'webdeveloper,development,porfolio,developer,senior,php,laravel,python,vuejs,aws,javascript',
  })
  const experienices = [
    {
      company: 'Bits Americas SAS',
      position: 'Technical Lead IV',
      time: 'Sep 2025 - Present',
      description: ''
    },
    {
      company: 'Sigaweb SAS',
      position: 'Lead Laravel & Vue Developer',
      time: 'Sep 2019 - Apr 2022',
      description: ''
    },
    {
      company: 'IT Makers',
      position: 'Backend Developer',
      time: 'Jan 2018 - Dec 2019',
      description: ''
    },
    {
      company: 'Ardem SAS',
      position: 'PHP & JavaScript Developer',
      time: 'Sep 2016 - Jan 2018',
      description: ''
    },
  ];

  const projects = [
    {
      title: 'Polyrics Labs',
      description: 'Polyrics Labs website, an initiative for the development of open-source, minimalist, and functional code.',
      coverImg: 'https://t2.genius.com/unsafe/344x344/https%3A%2F%2Fimages.genius.com%2Fb7aef36663862fcbb0ad08b9e3bf05a3.640x640x1.jpg',
      github: 'https://github.com/polyrico/Polyrics-Labs',
      website: 'https://polyrics.dev',
    },
    {
      title: 'Foundify',
      description: 'Marketplace-style platform for posting lost items.',
      github: 'https://github.com/orgs/Polyrics-Labs/repositories',
      website: 'https://foundify.polyrics.dev',
    },
    {
      title: 'My Home Cloud',
      description: 'My private cloud, accessible to everyone, PiHole, Plex, development services, VPN, and more.',
    },
    {
      title: 'CloudShare',
      description: 'Infinite cloud space, connecting all cloud service APIs to expand cloud space.',
    },
  ];
</script>