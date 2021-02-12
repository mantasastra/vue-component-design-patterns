<template>
  <button class="button"><slot>Submit</slot></button>
</template>

<script>
export default {
  name: "BaseButton",
};
</script>

<style scoped>
.button {
  padding: 0.5rem;
  margin: 0.5rem;
  color: #ffffff;
  background-color: #42b983;
  border: 1px solid #2c3e50;
  border-radius: 10px;
  text-transform: uppercase;
  font-weight: bold;
  transition: 0.3s ease-in;
  cursor: pointer;
}

.button:hover {
  opacity: 0.8;
}

.button:focus {
  outline: none;
}
</style>
