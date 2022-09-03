<template>
  <div id="app">
    <display-selection></display-selection>
    <dog-button></dog-button>
    <cat-button></cat-button>
  </div>
</template>

<script>
import axios from "axios"

import DogButton from '@/components/DogButton.vue'
import DisplaySelection from '@/components/DisplaySelection.vue'
import CatButton from '@/components/CatButton.vue'



axios
export default {
  components: {
    DisplaySelection,
    DogButton,
    CatButton
  },
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
