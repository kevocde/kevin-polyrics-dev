<template>
  <div class="fixed inset-x-0 bottom-0 flex justify-center gap-2 py-5">
    <a class="bg-white hover:bg-gray-200 p-3 rounded-full flex justify-center align-center" @click="prevPage">
      <svg class="w-4 h-fit" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000" height="800px" width="800px" version="1.1" id="Layer_1" viewBox="0 0 330 330" xml:space="preserve">
        <path id="XMLID_224_" d="M325.606,229.393l-150.004-150C172.79,76.58,168.974,75,164.996,75c-3.979,0-7.794,1.581-10.607,4.394  l-149.996,150c-5.858,5.858-5.858,15.355,0,21.213c5.857,5.857,15.355,5.858,21.213,0l139.39-139.393l139.397,139.393  C307.322,253.536,311.161,255,315,255c3.839,0,7.678-1.464,10.607-4.394C331.464,244.748,331.464,235.251,325.606,229.393z"></path>
      </svg>
    </a>
    <a class="bg-white hover:bg-gray-200 p-3 rounded-full flex justify-center align-center" @click="nextPage">
      <svg class="w-4 h-fit" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000" height="800px" width="800px" version="1.1" id="Layer_1" viewBox="0 0 330 330" xml:space="preserve">
        <path id="XMLID_225_" d="M325.607,79.393c-5.857-5.857-15.355-5.858-21.213,0.001l-139.39,139.393L25.607,79.393  c-5.857-5.857-15.355-5.858-21.213,0.001c-5.858,5.858-5.858,15.355,0,21.213l150.004,150c2.813,2.813,6.628,4.393,10.606,4.393  s7.794-1.581,10.606-4.394l149.996-150C331.465,94.749,331.465,85.251,325.607,79.393z"></path>
      </svg>
    </a>
  </div>
</template>

<script lang="ts" setup>
  const currentScrollY = ref(window.scrollY || 0);
  const props = defineProps({
    ids: {
      type: Array<string>,
      required: true
    }
  });

  // Computed properties
  

  // Definition of listeners
  document.addEventListener('scroll', (evt) => {
    currentScrollY.value = window.scrollY;
  });

  // Definition of events
  function nextPage() {
    let initial = 0;
    const cords = props.ids
      .map(id => {
        const cord =  document.getElementById(id)?.getBoundingClientRect() || { top: 0, bottom: 0, height: 100 };
        const top = initial;
        initial += cord.height;

        return {
          top,
          bottom: initial
        };
      })
    ;

    for (let idx in cords) {
      let cord = cords[idx];
      if (currentScrollY.value >= cord.top && currentScrollY.value < cord.bottom) {
        const nextId = (parseInt(idx) + 1 == cords.length) ? 0 : (parseInt(idx) + 1);
        window.scrollTo(0, cords[nextId].top);
        break;
      }
    }
  }

  function prevPage() {
    let initial = 0;
    const cords = props.ids
      .map(id => {
        const cord =  document.getElementById(id)?.getBoundingClientRect() || { top: 0, bottom: 0, height: 100 };
        const top = initial;
        initial += cord.height;

        return {
          top,
          bottom: initial
        };
      })
    ;

    for (let idx in cords) {
      let cord = cords[idx];
      if (currentScrollY.value >= cord.top && currentScrollY.value < cord.bottom) {
        const nextId = (parseInt(idx) == 0) ? (cords.length - 1) : parseInt(idx) - 1;
        window.scrollTo(0, cords[nextId].top);
        break;
      }
    }
  }
  
</script>

<style>

</style>