<template>
  <div class="review__list flex mb-14">
    <CommonCardReview
      v-for="(review, idx) in reviews"
      :author="review.author"
      :text="review.text"
      class="review__element relative"
      :class="{
        'active': (idx === reviewActive),
        'prev': (idx === reviewPrev),
        'next': (idx === reviewNext),
        'move_to_left': (reviewActive === ((reviews?.length || 0)-1)),
        'move_to_right': (reviewActive === 0)
      }"
      @click="focusOn($event, idx)"
    ></CommonCardReview>
  </div>
  <ul class="review__controls flex gap-4">
    <li v-for="n in ((reviews?.length || 1) - 1)"><button class="control border-2 border-emerald-400 p-2 rounded-full" :class="{'bg-emerald-400': ((n - 1) === reviewActive)}" @click="focusOn($event, (n-1))"></button></li>
  </ul>
</template>

<script lang="ts" setup>
  const props = defineProps({
    'reviews': {type: Array<any>, require: true},
  });

  let reviewActive = ref(0);
  let reviewPrev = ref(-1);
  let reviewNext = ref(1);
  const classObject = reactive({});

  const focusOn = (evt: Event, key: any) => {
    reviewActive.value = key;
    reviewNext.value = (key+1);
    reviewPrev.value = (key-1);

    if (reviewActive.value === ((props.reviews?.length || 0) - 1)) {
      document.querySelector('.active')?.classList.add('move-to-left')
    }

    if (reviewActive.value === 0) {
      document.querySelector('.active')?.classList.add('move-to-right')
    }
  }
</script>

<style>
  .review__list {
    min-height: 20rem;
  }

  .review__element {
    transform: scale(0.6);
    display: none;
    opacity: 0;
    transition: 1s;
  }

  .active {
    transform: scale(0.9) translateY(2rem);
    display: block;
    opacity: 1;
    z-index: 1;
  }

  .prev {
    transform: scale(0.8) translateY(-1rem) translate(39rem);
    display: block;
    opacity: 0.6;
  }

  .next {
    transform: scale(0.8) translateY(-1rem) translate(-39rem);
    display: block;
    opacity: 0.6;
  }

  .move_to_left {
    left: -10rem;
  }

  .move_to_right {
    left: 10rem;
  }

  .review__controls .control {
    content: " ";
  }

  @media (width >= 48rem) {
    .review__element {
      transform: scale(0.7);
    }

    .active {
      transform: scale(1) translateY(2rem);
    }

    .prev {
      transform: scale(0.9) translateY(-1rem) translate(39rem);
    }

    .next {
      transform: scale(0.9) translateY(-1rem) translate(-39rem);
    }
  }
</style>