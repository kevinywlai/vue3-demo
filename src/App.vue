<template>
  <div id="app">
    <h1>Reusable Input with Dynamic Max Length</h1>
    <InputWithMaxLength :initialMaxLength="15" />
  </div>
</template>

<script>
import InputWithMaxLength from "./views/InputWithMaxLength.vue";

export default {
  name: "App",
  components: {
    InputWithMaxLength,
  },
};
</script>


<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
