<script lang="ts">
export default {
  props: {
    showChannels: Boolean,
    toggleChannels: Function,
  }
};
</script>

<template>
  <div class="channelHeader" @click="toggleChannels">
    <div class="iconWrapper">
      <font-awesome-icon v-bind:class="['icon', showChannels ? 'icon-down' : 'icon-right']" icon="caret-down" size="1x"/>
    </div>
    <h2>Channels</h2>
  </div>
</template>

<style scoped>
.channelHeader {
  display: flex;
  flex-flow: row;
  align-items: center;
}

.icon {
  text-align: center
}

.icon-down {
  transform: rotate(0deg);
  transition: transform 50ms linear;
}
.icon-right {
  transform: rotate(-90deg);
  transition: transform 50ms linear;
}

.channelHeader > .iconWrapper:hover {
  background-color: #532753;
}

</style>
