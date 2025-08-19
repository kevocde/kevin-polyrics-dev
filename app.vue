<template>
  <SectionsMainNav></SectionsMainNav>
  <SectionsProfile id="profile"></SectionsProfile>
  <SectionsResume id="resume"></SectionsResume>
  <SectionsWorkingOn id="workingon"></SectionsWorkingOn>
  <SectionsExperiencie id="workexperience" :experiencies="experienices"></SectionsExperiencie>
  <SectionsContact id="contact"></SectionsContact>
  <SectionsFooter id="footer"></SectionsFooter>
</template>

<script setup>
  const experienices = [
    {
      company: 'Bits Americas SAS',
      position: 'Technical Lead IV',
      time: 'Sep 2025 - Present',
      description: 'Lorem Ipsum ....'
    },
    {
      company: 'Sigaweb SAS',
      position: 'Lead Laravel & Vue Developer',
      time: 'Sep 2019 - Apr 2022',
      description: 'Lorem Ipsum ....'
    },
    {
      company: 'IT Makers',
      position: 'Backend Developer',
      time: 'Jan 2018 - Dec 2019',
      description: 'Lorem Ipsum ....'
    },
    {
      company: 'Ardem SAS',
      position: 'PHP & JavaScript Developer',
      time: 'Sep 2016 - Jan 2018',
      description: 'Lorem Ipsum ....'
    },
  ];
</script>