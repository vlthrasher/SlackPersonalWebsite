<script setup lang="ts">
import SideBar from "./components/SideBar.vue";
import TheWelcome from "./components/TheWelcome.vue";
</script>

<template>
    <SideBar msg="You did it!" />

  <!-- <main>
    <TheWelcome />
  </main> -->
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
  flex-flow: row;
  align-self: stretch;
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

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

a:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}
</style>
