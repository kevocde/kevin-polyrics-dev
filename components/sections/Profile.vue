<template>
  <CommonResponsiveContainer class="profile bg-indigo-50">
    <div class="profile__cover flex justify-center px-4 mb-6">
      <div class="relative">
        <div class="cover__img rounded-full overflow-hidden outline outline-white outline-offset-2">
          <img class="w-40 md:w-48 xl:w-64" src="/profiles/1-1-profile.jpg" alt="">
          <span class="absolute bg-white rounded-full py-1 px-2 absolute text-md md:text-lg">I'm Kevin G 👋</span>
        </div>
      </div>
    </div>
    <div class="profile__slogan flex justify-center px-4 mb-12">
      <h2 class="slogan__text text-2xl text-center md:text-3xl xl:text-4xl">Connecting the world with <strong class="text-emerald-400">APIs</strong>, <strong class="text-emerald-400">Web Apps</strong>, and <strong class="text-emerald-400">Tools</strong> for everyone.</h2>
    </div>
    <div class="profile__controls flex justify-center px-4">
      <CommonButtom target="_blank" href="https://www.linkedin.com/in/kevocde" type="link" class="bg-indigo-400 hover:bg-indigo-500 hover:animation-shake">Contact Me ↗</CommonButtom>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>

</script>

<style lang="scss">
  .profile {
    padding-top: 10rem;
    padding-bottom: 10rem;

    .profile__cover .cover__img span {
      top: 5rem;
      right: -4rem;
      transform: rotate(-10deg);
    }
  }

  @media (width >= 48rem) {
    .profile {
      padding-top: 12.5rem;
      padding-bottom: 12.5rem;

      .profile__cover .cover__img span {
        top: 6rem;
        right: -6rem;
      }
    }
  }

  @media (width >= 80rem) {
    .profile {
      padding-top: 15rem;
      padding-bottom: 15rem;
    }
  }
</style>