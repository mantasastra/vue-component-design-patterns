<template>
  <div>
    <slot
      name="title"
      :bookTitle="bookTitle"
      :upperCaseTitle="upperCaseTitle"
    ></slot>
    <slot name="description" :description="description"></slot>
  </div>
</template>

<script>
export default {
  name: "Book",
  data() {
    return {
      bookTitle: "Harry Potter",
      description: "The best book ever written.",
    };
  },
  computed: {
    upperCaseTitle() {
      return this.bookTitle.toUpperCase();
    },
  },
};
</script>

<style scoped></style>
