<script lang="ts">
import ChannelButton from "./ChannelButton.vue";
export default {
  components: {
    ChannelButton
  },
  data() {
    return {
      channels: [
        { id: 'about-me' },
        { id: 'education' },
        { id: 'work' },
        { id: 'projects' }
      ],
      showChannels: true,
      selectedChannel: null,
    };
  },

  methods: {
    toggleChannels() {
      console.log("In toggle channels");
      this.showChannels = !this.showChannels
    },
    selectChannel(channelId: string) {
      console.log(`Select Channel: ${channelId}`);
      this.selectedChannel = channelId;
    },
  },
};
</script>

<template>
  <div class="sidebar">
    <h1>Vicky Thrasher</h1>
    <h2 @click="toggleChannels">Channels</h2>
    <template v-for="channel in channels">
      <ChannelButton
        v-if="showChannels || selectedChannel === channel.id"
        :id="channel.id"
        :selected="selectedChannel === channel.id"
        :selectChannel="selectChannel"
      />
    </template>
  </div>
</template>

<style scoped>
.sidebar {
  display: flex;
  flex-flow: column;
  color: #cfc3cf;
  background-color: #3e0e40;
  width: 250px;
  height: 100%;
  border-color: #573f57;
  border-width: 1px 1px 0px 0px;
  position: sticky;
  text-align: start;
}

.sidebar > * {
  text-align: start;
  width: 100%;
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
