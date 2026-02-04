<template>
  <section class="exercise-2" :class="customClass">
    <div class="exercise-2__wrapper">
      
      <div
        v-for="(item, index) in items"
        :key="index"
        class="exercise-2__item"
        :class="item.class">
        <component
          v-if="item.subtitle"
          :is="item.subtitleTag || 'h3'"
          class="exercise-2__subtitle">
          {{ item.subtitle }}
        </component>

        <component
          v-if="item.title"
          :is="item.titleTag || 'h2'"
          class="exercise-2__title">
          {{ item.title }}
        </component>

        <div class="exercise-2__video">
          <iframe
            :src="item.url"
            frameborder="0"
            allow="autoplay; fullscreen; picture-in-picture"
            allowfullscreen>
          </iframe>
        </div>
      </div>

    </div>
  </section>
</template>



<script>
// //import gsap from 'gsap';
export default {
  name: 'Exercise-2',
  props: {
  customClass: {
    type: String,
    default: ''
  },
  items: {
    type: Array,
    required: true
  }
 }
}

document.addEventListener("DOMContentLoaded", () => {
    console.log('Exercise 2 loaded');
});

</script>


<style scoped>

.exercise-2 {
    border: 5px solid gray;
}

.exercise-2__video {
  position: relative;
  padding-bottom: 50%;
  height: 0;
  overflow: hidden;
}

.exercise-2__video iframe {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
}

</style>