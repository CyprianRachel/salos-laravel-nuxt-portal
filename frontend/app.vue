<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
import { useAuthStore } from "~/stores/auth";
import { onMounted } from "vue";

const authStore = useAuthStore();

onMounted(() => {
  authStore.loadAuthData(); // Ładowanie tokena i danych użytkownika przy starcie aplikacji
});
</script>
