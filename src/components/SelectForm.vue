<script setup>
defineProps({
  title: String,
  placeholder: String,
  values: Array,
});

console.log();
</script>
<template>
  <label>
    <p>Hudud</p>
    <select>
      <option value="any" disabled hidden selected>{{ placeholder }}</option>
      <option v-for="value in values" :value="value.value">
        {{ value.name }}
      </option>
    </select>
  </label>
</template>
