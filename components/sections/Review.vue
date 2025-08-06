<template>
  <CommonResponsiveContainer class="bg-white review py-12 mb-20">
    <div class="review__title px-4 mb-20 text-center">
      <h3 class="text-4xl">Reviews</h3>
      <p class="text-gray-500 text-md">My colleagues from different companies say</p>
    </div>
    <div class="review__body px-4 flex flex-col items-center justify-center">
      <CommonReviewCarousel :reviews="reviews"></CommonReviewCarousel>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
  const reviews = [
    {
      author: 'Mauricio Galindo',
      text: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit',
      profile: '',
      position: ''
    },
    {
      author: 'Julio García',
      text: 'Veniam at, libero in velit accusamus laudantium amet rem pariatur nulla tempore voluptatum non officia rerum consectetur ipsam eveniet id atque adipisci?',
      profile: '',
      position: ''
    },
    {
      author: 'John Mendoza',
      text: 'Lorem ipsim at, libero in velit accu',
      profile: '',
      position: ''
    },
    {
      author: 'Camilo Sanchez',
      text: 'Me estoy moviendo un poquito',
      profile: '',
      position: ''
    },
    {
      author: 'Gabriel Murillo',
      text: 'De perico a tusi',
      profile: '',
      position: ''
    },
  ];
</script>

<style>
</style>