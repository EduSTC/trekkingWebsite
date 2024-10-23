<script setup>
import { RouterLink, RouterView } from 'vue-router'
import RobotaHeader from './components/RobotaHeader.vue'
import SensorsNavigation from './components/SensorsNavigation.vue'
import SensorsGraph from './components/SensorsGraph.vue'
</script>

<template>
  <header>
    <RobotaHeader></RobotaHeader>
  </header>
  <main>
    <SensorsNavigation></SensorsNavigation>
    <SensorsGraph></SensorsGraph>
  </main>

  <RouterView />
</template>

<style scoped>

</style>
