<template>
  <section>
    <img :src="image" alt="movie poster" />
    <h1>{{ title }}</h1>
    <p>{{ length }}</p>
    <span v-if="watched">✅</span>
  </section>
</template>

<script>
import placeholder from "@/assets/logo.png";

export default {
  name: "MoviePoster",
  props: {
    image: {
      type: String,
      default: placeholder,
    },
    title: {
      type: String,
      required: true,
    },
    length: {
      type: [Number, String],
      default: 90,
    },
    watched: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped></style>
