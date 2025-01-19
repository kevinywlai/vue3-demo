<template>
  <div>
    <label for="textInput">Enter text:</label>
    <input
      id="textInput"
      v-model="inputValue"
      :maxlength="maxLength"
      placeholder="Type something..."
    />
    <p>Max length: {{ maxLength }}</p>
    <p>Current length: {{ inputValue.length }}</p>
    <button @click="increaseMaxLength">Increase Max Length</button>
    <button @click="decreaseMaxLength">Decrease Max Length</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    // Reactive properties
    const inputValue = ref("");
    const maxLength = ref(10);

    const increaseMaxLength = () => {
      maxLength.value += 5; // Increase maxlength by 5
    };

    const decreaseMaxLength = () => {
      maxLength.value = Math.max(1, maxLength.value - 5); // Decrease maxlength but ensure it's at least 1
    };

    return {
      inputValue,
      maxLength,
      increaseMaxLength,
      decreaseMaxLength,
    };
  },
};
</script>

<style>
button {
  margin: 5px;
}
</style>
