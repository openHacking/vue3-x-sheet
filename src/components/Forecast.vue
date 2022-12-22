<script setup lang="ts">
import { onMounted } from "vue";

onMounted(() => {
  window.xsheet = new window.XSheet("#demo", {
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
