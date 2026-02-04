<template>
  <div
    class="exercise-1"
    :class="customClass"
    :style="bgimage ? { backgroundImage: `url(${bgimage})` } : null">
    <component :is="titleTag" class="exercise-1__title">
      {{ title }}
    </component>
    <a
      v-if="link && linkText"
      :href="link"
      :target="target"
      class="exercise-1__link">
      {{ linkText }}
    </a>
  </div>
</template>


<script>
// //import gsap from 'gsap';
export default {
  name: 'Exercise-1',
    props: {
        title: {
        type: String,
        required: true
        },
        titleTag: {
        type: String,
        default: 'h1'
        },
        link: {
        type: String,
        default: null
        },
        linkText: {
        type: String,
        default: null
        },
        target: {
        type: String,
        default: '_blank'
        },
        bgimage: {
        type: String,
        default: null
        },
        customClass: {
        type: String,
        default: null
        }
    }
}



document.addEventListener('DOMContentLoaded', () => {
  console.log('Exercise 1 loaded');
});

</script>


<style scoped >

.exercise-1 {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 5px solid gray;
}

/* .exercise-1__background-image::after, */
.exercise-1__background-image img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
}

/* .exercise-1__background-image::after {
  content: "";
  background-color: hsla(0, 0%, 0%, 0.4);
} */

.exercise-1__background-image img {
  object-fit: cover;
}

.exercise-1__container {
  max-width: var(--container-width);
}

.exercise-1__wrapper {
  position: relative;
  z-index: 1;
  text-align: center;
}

.exercise-1__title {
  display: inline-block;
  width: 100%;
}

</style>