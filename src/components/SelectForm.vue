<script setup>
defineProps({
  title: String,
  placeholder: String,
  values: Array,
});
console.log();
</script>
<template>
  <label class="wrapper-label">
    <p>{{ title }}</p>
    <select class="select">
      <option class="select-option" value="any" disabled hidden selected>{{ placeholder }}</option>
      <option class="select-option" v-for="value in values" :value="value.value">
        {{ value.name }}
      </option>
    </select>
  </label>
</template>
