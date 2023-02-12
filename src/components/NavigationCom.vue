<script setup>
import { ref } from "vue";
import navigation from "../data/navigation";

const openNav = ref(true);
</script>

<template>
  <nav class="navbar">
    <div class="nav-header">
      <img src="../assets/logo.png" alt="" />
      <p v-if="openNav">ERP-SPORT</p>
    </div>

    <div class="nav-content">
      <ul v-for="nav in navigation" class="nav-content-header">
        <p class="nav-content-title">{{ nav.name }}</p>

        <li v-for="link in nav.links" class="nav-content-link">
          <img src="../assets/icons/journal-bookmark-fill.svg" alt="" />
          <a :href="link.url">{{ link.name }}</a>
        </li>
      </ul>
    </div>

    <div class="nav-footer">
      <input type="checkbox" id="close-nav" />
      <label for="close-nav">
        <img src="../assets/icons/arrow-bar-left.svg" alt="left svg" />
      </label>
    </div>
  </nav>
</template>
