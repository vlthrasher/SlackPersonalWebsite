<script setup lang="ts">
import WorkspaceSideBar from "./WorkspaceSideBar.vue";
import SideBar from "./SideBar.vue";
</script>

<template>
  <div class="bodyContent">
    <WorkspaceSideBar />
    <SideBar msg="You did it!" />
  </div>
</template>

<style scoped>
body {
  display: flex;
  place-items: center;
}

.bodyContent {
  display: flex;
  flex: 1;
  flex-flow: row;
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