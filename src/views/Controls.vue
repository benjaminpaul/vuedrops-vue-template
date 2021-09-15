<template>
  <div>
    <div>
      <app-bar />
      <div class="home-hero">
        <page-container>
          <hero />
        </page-container>
      </div>
      <features />
      <channels />
      <signup />
    </div>
  </div>
</template>

<script>
import PageContainer from "@/components/PageContainer.vue";

import AppBar from "@/components/AppBar.vue";
import Hero from "./Home/components/Hero.vue";
import Features from "./Home/components/Features.vue";
import Channels from "./Home/components/Channels.vue";
import Signup from "./Home/components/Signup.vue";
export default {
  components: {
    PageContainer,
    Signup,
    AppBar,
    Hero,
    Features,
    Channels,
  },
};
</script>

<style lang="scss" scoped>
.home-hero {
  @apply bg-yellow-100;
}
</style>