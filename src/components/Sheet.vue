<script setup lang="ts">
import { onMounted } from "vue";

onMounted(() => {
  new window.XSheet("#demo", {
    workConfig: {
      body: {
        sheets: [window["forecast"]],
      },
    },
  });
});
</script>

<template>
  <div id="demo"></div>
</template>

<style scoped>
#demo {
  width: 100%;
  height: 100%;
}
</style>
