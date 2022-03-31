<template>
  <div>
    <form @submit.prevent="calculImc">
      <input
        type="number"
        v-model="imc.taille"
        name="taille"
        placeholder="Indiquer votre taille en cm"
        min="1"
        max="250"
        required
      />
      <input
        type="number"
        name="poids"
        v-model="imc.poids"
        placeholder="Indiquer votre poids en kg"
        min="1"
        max="400"
        required
      />
      <button>Calculer</button>
    </form>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";
import { useImcStore } from "@/stores/imc";

const imc = reactive({
  taille: 0,
  poids: 0,
});

const store = useImcStore();

function calculImc() {
  if (Number.isInteger(imc.poids && imc.taille)) {
    let calculateImc = Math.round(
      (imc.poids / Math.pow(imc.taille, 2)) * 10000
    );
    store.imc = calculateImc;
    store.taille = imc.taille;
    store.poids = imc.poids;
  } else {
    console.log("c'est pas un nombre mon reuf");
  }
}
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
form input {
  padding: 20px;
  width: 200px;
}
form button {
  width: 100px;
  padding: 10px;
}
</style>
