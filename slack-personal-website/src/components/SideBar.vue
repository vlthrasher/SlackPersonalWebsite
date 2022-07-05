<script lang="ts">
import ChannelButton from "./ChannelButton.vue";
import ChannelHeader from "./ChannelHeader.vue";
export default {
  components: {
    ChannelButton,
    ChannelHeader,
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
    <ChannelHeader
      :toggleChannels="toggleChannels"
      :showChannels="showChannels"
      />
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
  padding-left: 10px;
  padding-right: 10px;
  user-select: none;
}

.sidebar *:not(h1) {
  padding-top: 5px;
  padding-bottom: 5px;
}

.sidebar *:not(h1) > :nth-child(1) {
  border-radius: 4px;
  width: 1.75em;
  height: 1.75em;
  line-height: 1.75em;
  text-align: center;
}

.sidebar *:not(h1) :nth-child(2) {
  padding-left: 5px;
}


h1 {
  color: white;
  border-bottom-width: 1px;
  border-color: #573f57;
  font-weight: bold;
  font-size: 25px;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
