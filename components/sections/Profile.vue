<template>
  <CommonResponsiveContainer>
    <div class="profile-cmp flex justify-center relative pt-10 px-3 md:pt-20 md:mb-3 lg:pt-40 lg:mb-6">
      <div class="profile-cmp__container image rounded-full overflow-hidden w-32 outline outline-white outline-offset-2 mb-2 md:w-48">
        <img class="container__img" src="/profiles/1-1-profile.jpg" alt="">
      </div>
      <div class="profile-cmp__badge bg-white rounded-full px-3 py-1 cursor-pointer absolute right-0 bottom-4">
        <span class="badge__tag text-md font-medium md:text-lg">I'm Kevin G, 👋</span>
      </div>
    </div>
    <div class="slogan-cmp flex justify-center mb-6 px-4 md:mb-12 lg:px-12">
      <h2 class="slogan-cmp__text text-2xl text-center md:text-3xl lg:text-4xl">Connecting the world with <strong class="text-emerald-400">APIs</strong>, <strong class="text-emerald-400">Web Apps</strong>, and <strong class="text-emerald-400">Tools</strong> for everyone.</h2>
    </div>
    <div class="profile-cmp_buttons flex justify-center pb-10 md:pb-20 lg:pb-40">
      <CommonButtom target="_blank" href="https://www.linkedin.com/in/kevocde" type="link">Contact Me ↗</CommonButtom>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>

</script>

<style>
  .slogan-cmp__text {
    line-height: 2rem;
  }

  .profile-cmp__badge {
    transform: rotate(-10deg);
  }

  @media (width >= 48rem) {
    .profile-cmp__badge {
      right: 25vw;
      bottom: 10vw;
    }
  }

  @media (width >= 64rem) {
    .profile-cmp__badge {
      right: calc(1vw * 30.5);
      bottom: calc(1vw * 6.5);
    }
  }
</style>