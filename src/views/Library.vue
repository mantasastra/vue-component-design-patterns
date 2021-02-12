<template>
  <div>
    <Book>
      <!-- slotProps are scoped only to this template! -->
      <template v-slot:title="{ upperCaseTitle }">
        <h1>{{ upperCaseTitle }}</h1>
      </template>
      <template v-slot:description="{ description }">
        <p>{{ description }}</p>
      </template>
    </Book>
  </div>
</template>

<script>
import Book from "@/components/Book";

export default {
  name: "Library",
  components: {
    Book,
  },
};
</script>

<style scoped></style>
