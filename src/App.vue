<template>
  <controls />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Controls from "./views/Controls.vue";

export default defineComponent({
  name: "App",
  components: {
    Controls,
  },
});
</script>

<style lang="scss">
</style>
