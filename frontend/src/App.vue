<script setup>
import Catalog from './components/catalog/Catalog.vue'
import Navbar from './components/globals/Navbar.vue'
</script>

<template>
  <div>
    <div class="container-fluid">
      <Navbar />
    </div>
    <div class="container">
      <Catalog />
    </div>
  </div>
</template>
