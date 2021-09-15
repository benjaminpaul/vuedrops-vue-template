<template>
  <div class="channels">
    <h3>With Saaslify you can start<br />selling on all channels</h3>
    <div class="container mx-auto flex items-center justify-center mt-8">
      <div class="flex-1 p-16">
        <img src="@/assets/app_layout_4.svg" />
      </div>
      <div class="flex-1 p-16">
        <div class="channel-info">
          <div class="flex items-center justify-center" @click="toggleFacebook">
            <div><i class="fab fa-facebook text-5xl mr-8"></i></div>
            <div class="flex-1">
              <h4>Facebook</h4>
              <transition name="fade">
                <div v-if="facebookExpanded">
                  <p class="text-gray-500 mt-4">
                    Lorem ipsum dolor sit amet consectetur dor adipiscing elit
                    turpis viverra amet elit.
                  </p>
                </div>
              </transition>
            </div>
            <div><i class="fas fa-chevron-right text-3xl"></i></div>
          </div>
        </div>
        <div class="channel-info">
          <div
            class="flex items-center justify-center"
            @click="toggleInstagram"
          >
            <div><i class="fab fa-instagram text-5xl mr-8"></i></div>
            <div class="flex-1">
              <h4>Instagram</h4>
              <transition name="fade">
                <div v-if="instagramExpanded">
                  <p class="text-gray-500 mt-4">
                    Lorem ipsum dolor sit amet consectetur dor adipiscing elit
                    turpis viverra amet elit.
                  </p>
                </div>
              </transition>
            </div>
            <div><i class="fas fa-chevron-right text-3xl"></i></div>
          </div>
        </div>
        <div class="channel-info">
          <div class="flex items-center justify-center" @click="toggleGoogle">
            <div><i class="fab fa-google text-5xl mr-8"></i></div>
            <div class="flex-1">
              <h4>Google Shopping</h4>
              <transition name="slide">
                <div v-if="googleExpanded">
                  <p class="text-gray-500 mt-4">
                    Lorem ipsum dolor sit amet consectetur dor adipiscing elit
                    turpis viverra amet elit.
                  </p>
                </div>
              </transition>
            </div>
            <div><i class="fas fa-chevron-right text-3xl"></i></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const facebookExpanded = ref(false);
    const instagramExpanded = ref(false);
    const googleExpanded = ref(false);
    const toggleFacebook = () => {
      facebookExpanded.value = !facebookExpanded.value;
    };
    const toggleInstagram = () => {
      instagramExpanded.value = !instagramExpanded.value;
    };
    const toggleGoogle = () => {
      googleExpanded.value = !googleExpanded.value;
    };
    return {
      facebookExpanded,
      instagramExpanded,
      googleExpanded,
      toggleFacebook,
      toggleInstagram,
      toggleGoogle,
    };
  },
};
</script>

<style lang="scss" scoped>
.channels {
  @apply mx-auto bg-blue-50 pt-16 pb-16;
  h3 {
    @apply text-center;
  }
  .channel-info {
    @apply p-8 border border-gray-200 rounded-lg mb-4 bg-white shadow-lg text-blue-900;
    cursor: pointer;
    transition: all 0.3s;
  }
  .channel-info:hover {
    @apply border-gray-400 shadow-none;
  }
}
.slide-enter-active {
  -moz-transition-duration: 0.3s;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -moz-transition-timing-function: ease-in;
  -webkit-transition-timing-function: ease-in;
  -o-transition-timing-function: ease-in;
  transition-timing-function: ease-in;
}

.slide-leave-active {
  -moz-transition-duration: 0.3s;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -moz-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  -webkit-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  -o-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
}

.slide-enter-to,
.slide-leave {
  max-height: 100px;
  overflow: hidden;
}

.slide-enter,
.slide-leave-to {
  overflow: hidden;
  max-height: 0;
}
</style>