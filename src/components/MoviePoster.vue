<template>
  <section>
    <img :src="image" alt="movie poster" />
    <h1>{{ title }}</h1>
    <p>{{ length }}</p>
    <span v-if="watched">✅</span>
  </section>
</template>

<script>
import placeholder from "@/assets/img/logo.png";

export default {
  name: "MoviePoster",
  props: {
    image: {
      type: String,
      default: placeholder,
      validator: (propValue) => {
        const hasImageDirectory = propValue.indexOf("/img/") > -1;
        const isPNG = propValue.endsWith(".png");
        const isJPEG =
          propValue.endsWith(".jpeg") || propValue.endsWith(".jpg");
        const hasValidExtension = isPNG || isJPEG;

        return hasImageDirectory && hasValidExtension;
      },
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
