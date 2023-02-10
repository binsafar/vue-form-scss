<script setup>
import { ref } from "vue";
const openNav = ref(true);
</script>

<template>
  <nav class="navbar">
    <div class="nav-header">
      <img src="../assets/logo.png" alt="" />
      <p v-if="openNav">ERP-SPORT</p>
    </div>
    <div class="nav-content"></div>
    <div class="nav-footer">
      <img src="../assets/icons/arrow-bar-left.svg" alt="left svg" />
    </div>
  </nav>
</template>
