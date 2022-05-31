<script>
    import { defineComponent } from "vue";
    import Popper from "vue3-popper";

export default defineComponent({
  components: {
    Popper,
  },
});
</script>

<template>
  <div class="workspaceIconWrapper">
    <Popper content="Vicky Thrasher" placement="auto-end" arrow="true" hover="true">
      <img alt="Vicky Logo" src="../assets/VInc.jpg" />
    </Popper>
  </div>
</template>

<style>
:root {
  --popper-theme-background-color: black;
  --popper-theme-background-color-hover: black;
  --popper-theme-text-color: white;
  --popper-theme-border-radius: 6px;
  --popper-theme-padding: 10px;
}

.popper {
  font-weight: bold;
  width: 135px;
}
</style>

<style scoped>
.workspaceIconWrapper {
  display: flex;
  flex-flow: column;
  align-self: flex-start;
  align-items: center;
  border-radius: .5em;
  border-color: white;
  border-width: 3px;
  padding: 4px;
}

img {
    border-radius: .5em;
}
</style>