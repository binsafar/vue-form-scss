<script setup>
import { ref } from "vue";
import SelectForm from "./SelectForm.vue";

let tableType = "shgh";
const customValues = ref([
  { id: 1, name: "Test", value: "Value1" },
  { id: 2, name: "Test", value: "Value1" },
  { id: 3, name: "Test", value: "Value1" },
  { id: 4, name: "Test", value: "Value1" },
]);

function changeState(state) {
  tableType = state;
  console.log(tableType);
}
</script>

<template>
  <div class="bank-container">
    <div class="bank-module">
      <button
        @click="changeState('shgh')"
        :class="(tableType = 'shgh' ? 'active' : '')"
      >
        SHG`H
      </button>
      <button
        @click="changeState('ixtisos')"
        :class="tableType == 'ixtisos' ? 'active' : ''"
      >
        Ixtisoslashtirilgan fanlar
      </button>
      <button
        @click="changeState('sport')"
        :class="tableType == 'sport' ? 'active' : ''"
      >
        Sport turlari
      </button>
    </div>

    <table class="bank-table">
      <!-- header -->
      <thead class="bank-thead">
        <!-- the form -->
        <tr class="bank-tr">
          <th><input class="bank-tr-input" type="text" /></th>
          <th><input class="bank-tr-input" type="text" /></th>
          <th>
            <SelectForm
              placeholder="Quyidagilarni tanlang"
              :values="customValues"
            />
          </th>
          <th>
            <label class="switch">
              <input id="new-con" type="checkbox" class="new-con" />
              <span class="slider round"></span>
            </label>
          </th>
          <th><SelectForm placeholder="Active" :values="customValues" /></th>
          <th><button class="btn-add">+ Qo'shish</button></th>
        </tr>
        <!-- description -->
        <tr class="bank-tr">
          <th>Hisob raqam</th>
          <th>Hisob raqam nomi</th>
          <th>Bank</th>
          <th>Odatiy</th>
          <th>Holati</th>
          <th>Amallar</th>
        </tr>
      </thead>
      <!-- body -->
      <tbody></tbody>
    </table>
  </div>
</template>
