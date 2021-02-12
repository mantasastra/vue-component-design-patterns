<template>
  <div class="home">
    <MoviePoster
      :image="logo"
      title="Framework"
      length="42:24"
      watched="true"
    />
  </div>
</template>

<script>
import MoviePoster from "@/components/MoviePoster";
import logo from "@/assets/logo.png";

export default {
  name: "Home",
  components: {
    MoviePoster,
  },
  data() {
    return {
      logo,
    };
  },
};
</script>
