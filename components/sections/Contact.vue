<template>
  <CommonResponsiveContainer class="contact py-20">
    <div class="title px-4 text-center">
      <h4 class="text-4xl">Contact Me</h4>
      <p class="text-gray-500 text-md">Need a hand?</p>
    </div>
    <ul class="links flex gap-4 justify-center px-4 py-10">
      <li>
        <a href="https://www.linkedin.com/in/kevocde" class="flex text-gray-600"><i class="mr-2"><img src="/icons/linkedin.svg" class="w-6 accent-color"></img></i>LinkedIn</a>
      </li>
      <li><a href="mailto:kevocde@gmail.com" class="flex text-gray-600"><i class="mr-2"><img src="/icons/maildotru.svg" class="w-6 accent-color"></img></i>Mail</a></li>
    </ul>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>

</script>

<style scoped>
  .accent-color {
    filter: invert(49%) sepia(7%) saturate(782%) hue-rotate(182deg) brightness(89%) contrast(99%);
  }
</style>