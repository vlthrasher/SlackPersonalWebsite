<script lang="ts">
export default {
  props: {
    id: String,
    selected: Boolean,
    selectChannel: Function,
  },
};
</script>

<template>
  <button class="channel" :class="{active: selected}" @click="selectChannel(id)">{{id}}</button>
</template>

<style scoped>
.channel {
  padding: 10px 35px;
}

.active {
  color: white;
  background-color: #1064a3;
}
</style>