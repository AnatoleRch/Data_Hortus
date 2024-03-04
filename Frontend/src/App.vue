<template>
  <v-app>
  <!-- une barre de navigation -->
  <v-app-bar
  color="primary"
  density="compact"
  >
  <!-- mettre l'icone dans le 'slot prepend' de 'v-app-bar' soit au début à gauche -->
  <template v-slot:prepend>
  <!-- un clic sur l'icone cache/affiche la zone de menu de gauche -->
  <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
  </template>
  <!-- le titre de la barre de navigation -->
  <v-app-bar-title>Application recherche films</v-app-bar-title>
  <!-- un simple bouton qui retourne à la page d'accueil route="/"-->
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
</style>