<template>
  <div>
    <table>
      <thead>
        Votre Imc est de
        {{
          store.imc
        }}
        👍
      </thead>
      <tr>
        <th>Poids</th>
        <th>Taille</th>
        <th>Indice de Masse Corporelle</th>
      </tr>
      <tr>
        <td>{{ store.taille }} cm</td>
        <td>{{ store.poids }} kg</td>
        <td>{{ store.imc }}</td>
      </tr>
    </table>
  </div>
</template>

<script setup lang="ts">
import { useImcStore } from "@/stores/imc";
const store = useImcStore();
</script>

<style scoped>
table {
  margin: 20px;
}
table,
th,
td {
  border: 1.5px solid black;
  padding: 10px;
  width: 700px;
}
</style>
