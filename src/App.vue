<script setup>
import HeaderCom from "./components/HeaderCom.vue";
import NavigationCom from "./components/NavigationCom.vue";
import OrgForm from "./components/OrgForm.vue";
</script>

<template>
  <div class="main-container">
    <NavigationCom />
    <div class="main-right">
      <HeaderCom />
      <OrgForm />
    </div>
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
}
.main-right {
  width: 82%;
}
@media (width < 1120px) {
  .main-right {
    width: 100%;
  }
}
</style>
