<script setup>
import { ref } from "vue";

const organization = ref({
  name: '"O`ZBEKISTON RESPUBLIKASI SPORTNI RIVOJLANTIRISH VAZIRLIGI" (323456789)',
  login: "admin",
  module: "Администратор",
});
</script>

<template>
  <header class="header" id="main-header">
    <label for="check-box" class="checkbox-icon">
      <img src="../assets/icons/list.svg" alt="list" />
    </label>

    <input type="checkbox" id="check-box" />

    <h1>SportERP</h1>

    <div class="header-info">
      <p class="header-org-title">
        <span class="header-org-span">Tashkilot:</span> {{ organization.name }}
      </p>
      <section class="header-org-info">
        <p>
          <span class="header-org-span">Foydalanuvchi (Login):</span>
          {{ organization.login }}
        </p>
        <p>
          <span class="header-org-span">Modul:</span> {{ organization.module }}
        </p>
      </section>
    </div>

    <div class="header-icon">
      <img class="right" src="../assets/icons/search.svg" alt="search icon" />
      <img class="right" src="../assets/icons/globe2.svg" alt="globa lang" />
      <img src="../assets/icons/person-circle.svg" alt="user avatar" />
    </div>
  </header>
</template>
