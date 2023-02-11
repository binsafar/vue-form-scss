<script setup>
import { ref } from "vue";
import SelectForm from "./SelectForm.vue";

const tableType = ref("shgh");
const customValues = ref([
  { id: 1, name: "Test", value: "Value1" },
  { id: 2, name: "Test", value: "Value1" },
  { id: 3, name: "Test", value: "Value1" },
  { id: 4, name: "Test", value: "Value1" },
]);
</script>

<template>
  <div>
    <button
      @click="tableType = 'shgh'"
      :class="tableType === 'shgh' ? 'active' : ''"
    >
      SHG`H
    </button>
    <button
      @click="tableType = 'ixtisos'"
      :class="tableType === 'ixtisos' ? 'active' : ''"
    >
      Ixtisoslashtirilgan fanlar
    </button>
    <button
      @click="tableType = 'sport'"
      :class="tableType === 'sport' ? 'active' : ''"
    >
      Sport turlari
    </button>
  </div>

  <table v-if="(tableType = 'shgh')">
    <thead>
      <tr>
        <th><input type="text" /></th>
        <th><input type="text" /></th>
        <th>
          <SelectForm
            placeholder="Quyidagilarni tanlang"
            :values="customValues"
          />
        </th>
        <th><SelectForm /></th>
        <th><button>+ Qo'shish</button></th>
      </tr>
      <tr>
        <th>Hisob raqam</th>
        <th>Hisob raqam nomi</th>
        <th>Bank</th>
        <th>Odatiy</th>
        <th>Holati</th>
        <th>Amallar</th>
      </tr>
    </thead>
    <tbody></tbody>
  </table>
</template>
