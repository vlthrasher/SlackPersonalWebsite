<script setup lang="ts">
import HeaderBar from "./components/HeaderBar.vue";
import BodyContent from "./components/BodyContent.vue";
</script>

<template>
  <HeaderBar />
  <BodyContent />
</template>

<style>
@import "./assets/base.css";

body {
  display: flex;
  place-items: center;
}

#app {
  display: flex;
  flex: 1;
  flex-flow: column;
  align-self: stretch;
  justify-content: flex-start;
}

header {
  line-height: 1.5;

  display: flex;
  place-items: center;
  padding-right: calc(var(--section-gap) / 2);
}

.logo {
  display: block;
  margin: 0 2rem 0 0;
}

a:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}
</style>
