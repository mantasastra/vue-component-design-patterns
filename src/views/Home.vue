<template>
  <div class="home">
    <CustomLayout>
      <template #header><p>Header content</p></template>
      <template
        ><MoviePoster :image="logo" title="Framework" length="42:24" watched />
        <BaseButton>Cancel something <span>or not</span></BaseButton>
        <BaseButton
      /></template>
      <!-- #footer === v-slot:footer -->
      <template v-slot:footer><p>Footer content</p></template>
    </CustomLayout>
  </div>
</template>

<script>
import MoviePoster from "@/components/MoviePoster";
import CustomLayout from "@/components/CustomLayout";
import BaseButton from "@/components/BaseButton";

import logo from "@/assets/img/logo.png";

export default {
  name: "Home",
  components: {
    MoviePoster,
    CustomLayout,
    BaseButton,
  },
  data() {
    return {
      logo,
    };
  },
};
</script>
