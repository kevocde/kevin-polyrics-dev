<template>
  <div class="review_card bg-gray-50 rounded-lg overflow-hidden w-80 shadow-md">
    <div class="card__body p-4 text-gray-500 text-lg h-80">
      <span class="body__double reverse text-2xl"><i class="lni lni-double-quotes-end-1"></i></span>
      {{ text }}
      <span class="body__double text-2xl"><i class="lni lni-double-quotes-end-1"></i></span>
    </div>
    <div class="card__footer bg-indigo-500 text-indigo-50 py-2 px-4">
      <div class="footer__profile bg-transparent flex gap-3">
        <div class="profile__img bg-white rounded-full">
          <div class="w-14">
            <img src="~/public/profiles/mauricio-galindo.png" alt=""></img>
          </div>
        </div>
        <div class="profile__text flex flex-col justify-center">
          <p class="text-md">{{ author }}</p>
          <span class="text-sm">Lead Manager at Millicom</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
  defineProps({
    author: {type: String},
    text: {type: String},
    profile: {type: String},
    position: {type: String},
  })
</script>

<style>
  .reverse i {
    transform: scale(-1);
    line-height: 0;
  }
</style>