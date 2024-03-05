<template>
  <v-app>
  <!-- une barre de navigation -->
  <v-app-bar
  color="primary"
  density="compact">
  <v-img
  :height="100"
  aspect-ratio="1/1"
  src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
  ></v-img>
  <v-btn to="/">Home</v-btn>
  <v-btn to="/Serre">S</v-btn>
  <v-btn to="/Pilotage">P</v-btn>
  <v-btn to="/Historique">H</v-btn>

</v-app-bar>

<!-- la zone où sera affichée les différentes "pages"-->
<v-main>
<v-container class="page">
<!-- les "composant view" s'afficheront ici -->
<RouterView />
</v-container>
</v-main>
</v-app>
</template>


<script setup>
</script>


<style scoped>
.page{
text-align: center;
}
v-img{
  float: left
}
</style>