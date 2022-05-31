<script setup lang="ts">
defineProps<{
  msg: string;
}>();
</script>

<template>
  <div class="sidebar">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a target="_blank" href="https://vitejs.dev/">Vite</a> +
      <a target="_blank" href="https://vuejs.org/">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
.sidebar {
  display: flex;
  flex-flow: row;
  background-color: #3e0e40;
  max-width: 20%;
  height: 100%;
  border-color: #573f57;
  border-width: 1px 1px 0px 0px;
  z-index: -1;
  position: sticky;
}

h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: left;
}
</style>
