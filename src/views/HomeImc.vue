<script setup lang="ts">
import FormImc from "../components/FormImc.vue";
import Table1 from "../components/Table.vue";
</script>

<template>
  <main>
    <h1>Calculateur d’IMC</h1>
    <section>
      <p>
        L’indice de masse corporelle (IMC) permet d’évaluer rapidement votre
        corpulence simplement avec votre poids et votre taille, quel que soit
        votre sexe. Calculez rapidement votre IMC et découvrez dans quelle
        catégorie vous vous situez.
      </p>
      <FormImc />
    </section>
    <Table1 />
  </main>
</template>

<style>
h1 {
  text-align: center;
}
section {
  display: flex;
  gap: 20px;
  justify-content: center;
}
section p {
  width: 20%;
}
main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 50px;
}
.hiddenTable {
  display: none;
}
</style>
