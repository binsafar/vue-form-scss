<script setup>
import { ref } from "vue";

const organization = ref({
  name: '"O`ZBEKISTON RESPUBLIKASI SPORTNI RIVOJLANTIRISH VAZIRLIGI" (323456789)',
  login: "admin",
  module: "Администратор",
});
</script>

<template>
  <header class="header">
    <input type="checkbox" />
    <div class="header-info">
      <p>Организация : {{ organization.name }}</p>
      <p>Имя пользователя : {{ organization.login }}</p>
      <p>Модуль :{{ organization.module }}</p>
    </div>
  </header>
</template>
