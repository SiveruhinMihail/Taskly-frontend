<script setup>
import { NuxtLayout } from "#components";
import { onMounted } from "vue";

const authStore = useAuthStore();

onMounted(() => {
  authStore.initTokens();
});
</script>

<template>
  <div class="app" style="font-family: JetBrainsMonoNL">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<style>
@import url("./assets/css/index.css");
@font-face {
  font-family: "JetBrainsMonoNL";
  src: url("/fonts/JetBrainsMonoNL-Regular.ttf");
}
</style>
