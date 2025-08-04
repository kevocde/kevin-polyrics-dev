<template>
  <CommonResponsiveContainer>
    <div class="mobile-nav md:hidden" v-bin="$attrs">
      <nav class="nav overflow-hidden relative">
        <a href="mailto:kevind.guzmand@gmail.com" class="nav__logo p-4 text-2xl leading-[0] block"><i class="lni lni-envelope-1"></i></a>
        <ul class="nav__links text-end" :class="{'hidden': !mobileMenuShow}">
          <li class="links__item"><a href="#resume" class="block px-4 py-2 cursor-pointer">Resume</a></li>
          <li class="links__item"><a href="#workingon" class="block px-4 py-2 cursor-pointer">Working On</a></li>
          <li class="links__item"><a href="#reviews" class="block px-4 py-2 cursor-pointer">Reviews</a></li>
        </ul>
        <a href="#" class="nav__toggle p-4 text-2xl leading-[0] block absolute right-0 top-0" @click="toggleMobileMenu">
          <i class="lni lni-menu-hamburger-1" v-if="!mobileMenuShow"></i>
          <i class="lni lni-xmark" v-if="mobileMenuShow"></i>
        </a>
      </nav>
    </div>
    <div class="normal-nav hidden md:block">
      <div class="nav overflow-hidden flex justify-between">
        <a href="mailto:kevind.guzmand@gmail.com" class="nav__logo p-4 text-2xl leading-[0] block"><i class="lni lni-envelope-1"></i></a>
        <ul class="nav__links text-end flex">
          <li class="links__item"><a href="#resume" class="block p-4 cursor-pointer underline underline-offset-2">Resume</a></li>
          <li class="links__item"><a href="#workingon" class="block p-4 cursor-pointer underline underline-offset-2">Working On</a></li>
          <li class="links__item"><a href="#reviews" class="block p-4 cursor-pointer underline underline-offset-2">Reviews</a></li>
        </ul>
      </div>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
  let mobileMenuShow = ref(false);

  const toggleMobileMenu = () => {
    mobileMenuShow.value = !mobileMenuShow.value;
  }
</script>

<style>

</style>