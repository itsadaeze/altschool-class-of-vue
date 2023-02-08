<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { colorPickerGame } from "../composables/color-picker.js";



export default {
setup() {
  const colorgame = colorPickerGame()
return {
  colors: colorgame.colors,
  message: colorgame.message,
  matchColor: colorgame.matchColor,
};
},

};
</script>

<style></style>