<script setup lang="ts">
import { ref } from 'vue';


const txt = ref('copy code')
function copyBtnCode() {
  navigator.clipboard.writeText('<a href="https://takedoor.neocities.org/"><img src="https://takedoor.neocities.org/button-neocities.gif" /></a>').then(
      function () {
        txt.value = "Copied"
      },
      function () {
        txt.value = "Error :/"
      },
  );
}
</script>

<template>
  <h1>ça c'est mon bouton</h1>
  <div>
  <a href="https://takedoor.neocities.org/">
    <img src="/button-neocities.gif" />
  </a>
  <button @click="copyBtnCode" id="copy-btn">{{ txt }}</button>
  </div>
</template>

<style scoped>

</style>