<script setup lang="ts">
defineProps<{
  msg: string;
}>();
</script>

<template>
  <div class="sidebar">
    <h1>Vicky Thrasher</h1>
  </div>
</template>

<style scoped>
.sidebar {
  display: flex;
  flex-flow: column;
  background-color: #3e0e40;
  width: 250px;
  height: 100%;
  border-color: #573f57;
  border-width: 1px 1px 0px 0px;
  z-index: -1;
  position: sticky;
}

.sidebar > * {
  padding: 10px 20px;
}

h1 {
  color: white;
  border-bottom-width: 1px;
  border-color: #573f57;
  font-weight: bold;
  font-size: 25px;
}
</style>
