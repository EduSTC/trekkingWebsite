<script setup>
import { RouterLink, RouterView } from 'vue-router'
import RobotaHeader from './components/RobotaHeader.vue'
</script>

<template>
  <header>
    <RobotaHeader></RobotaHeader>
  </header>

  <RouterView />
</template>

<style scoped>

</style>
