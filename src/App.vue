<script setup lang="ts">
import { onMounted } from 'vue';


onMounted(() => {
  document.documentElement.setAttribute('data-theme', 'light');
});

</script>

<template>
  <router-view />
</template>

<style src="./style.scss" />