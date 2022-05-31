<script setup lang="ts">
import Workspace from "./Workspace.vue";
</script>

<template>
  <div class="workspaceSideBar">
    <Workspace />
  </div>
</template>

<style scoped>
.workspaceSideBar {
  display: flex;
  position: sticky;
  background-color: #3e0e40;
  width: 80px;
  height: 100%;
  border-color: #573f57;
  border-width: 1px 1px 0px 0px;
  padding: 15px 10px;
}
</style>