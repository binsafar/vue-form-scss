<script setup>
import SelectForm from "./SelectForm.vue";
import { ref } from "vue";
import BankAcc from "./BankAcc.vue";

const customValues = ref([
  { id: 1, name: "Test", value: "Value1" },
  { id: 2, name: "Test", value: "Value1" },
  { id: 3, name: "Test", value: "Value1" },
  { id: 4, name: "Test", value: "Value1" },
]);

const submit = () => console.log("submit");
</script>
<template>
  <div class="form-container">
    <h1>Tashkilot</h1>

    <form @submit.prevent="submit" class="form-wrapper">
      <label>
        INN
        <input placeholder="INN" type="text" />
      </label>
      <label>
        Qisqa nomlanishi
        <input placeholder="Qisqa nomlanishi" type="text" />
      </label>
      <label>
        To`liq nomi
        <input placeholder="To`liq nomi" type="text" />
      </label>
      <label>
        Manzil
        <input placeholder="Manzil" type="text" />
      </label>
      <label>
        Indeks
        <input placeholder="Indeks" type="text" />
      </label>
      <label>
        Telefon
        <input placeholder="Telefon" type="text" />
      </label>
      <label>
        Direktor
        <input placeholder="Direktor" type="text" />
      </label>
      <label>
        Hisobchi
        <input placeholder="Hisobchi" type="text" />
      </label>
      <label>
        Iqtisodchi
        <input placeholder="Iqtisodchi" type="text" />
      </label>
      <label>
        Veb sayt
        <input placeholder="Veb sayt" type="text" />
      </label>
      <label>
        Ta`sis hujjati
        <input placeholder="Ta`sis hujjati" type="text" />
      </label>
      <label>
        Tashkil qilingan sa'na
        <input
          placeholder="Tashkil qilingan sa'na"
          type="text"
          onfocus="(this.type='date')"
        />
      </label>
      <label>
        Quvvati
        <input placeholder="Quvvati" type="text" />
      </label>
      <label>
        Koeffisient
        <input placeholder="Koeffisient" type="text" />
      </label>
      <!-- 3ta select -->
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />

      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />

      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />

      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />
      <SelectForm
        title="Hudud"
        placeholder="Hududni tanlang"
        :values="customValues"
      />

      <p>
        Yangi ta`mirlangan
        <label class="switch">
          <input id="new-con" type="checkbox" class="new-con" />
          <span class="slider round"></span>
        </label>
      </p>
    </form>

    <BankAcc />

    <div class="buttons">
      <button class="btn-cancel">Orqaga</button>
      <button class="btn-submit" @submit="submit">Saqlash</button>
    </div>
  </div>
</template>

<style scoped></style>
