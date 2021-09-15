<template>
  <div class="app-bar">
    <div class="container mx-auto">
      <div class="flex items-center justify-center">
        <div class="brand">
          <p>Saaslify X</p>
        </div>
        <div class="flex-1">
          <div class="menu-links">
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Features</a>
          </div>
        </div>
        <div class="menu-toggle">
          <i class="fas fa-bars" @click="toggleMenu"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const menuIsOpen = ref(false);
    const toggleMenu = () => {
      menuIsOpen.value = !menuIsOpen.value;
    };
    return {
      menuIsOpen,
      toggleMenu,
    };
  },
};
</script>

<style lang="scss" scoped>
.app-bar {
  @apply p-8 bg-yellow-100 text-blue-900;
  top: 0;
  left: 0;
  right: 0;
  .brand {
    p {
      @apply text-2xl font-bold mr-16;
    }
  }
  .menu-links {
    a {
      @apply mr-8 font-bold;
      transition: all 0.3s;
    }
    a:hover {
      @apply text-green-400;
    }
  }
  .menu-toggle {
    cursor: pointer;
  }
}
</style>