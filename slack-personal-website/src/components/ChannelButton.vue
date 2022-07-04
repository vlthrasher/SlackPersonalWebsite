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
  <div class="channel" :class="{active: selected}" @click="selectChannel(id)">
    <div class="hashtag">#</div>
    <button>{{id}}</button>
  </div>
</template>

<style scoped>
.channel {
  display: flex;
  flex-flow: row;
  align-items: center;
}

.channel > .hashtag {
  margin-right: 15px;
}

.active {
  color: white;
  background-color: #1064a3;
}
</style>