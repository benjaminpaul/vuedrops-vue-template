<template>
  <div
    class="
      rounded-xl
      bg-blue-900
      p-12
      m-14
      flex
      items-center
      justify-center
      ripple-background
    "
  >
    <div class="flex-1 p-8 relative">
      <h2 class="text-white">Sign up and create your online store today!</h2>
      <p class="text-gray-400 mt-4">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit convallis libero
        ac aliquet nibh et.
      </p>
    </div>
    <div class="flex-1 flex justify-center items-center">
      <div class="mx-auto">
        <button class="button mr-4">Start free trial</button
        ><button class="button-outline">Learn more</button>
      </div>
    </div>
    <div class="bg"></div>
    <div class="bg bg2"></div>
    <div class="bg bg3"></div>
  </div>
</template>

<style lang="scss" scoped>
.bg {
  animation: slide 3s ease-in-out infinite alternate;
  background-image: linear-gradient(-60deg, #6c3 50%, #09f 50%);
  opacity: 0.5;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -100;
  z-index: 10000;
}

.bg2 {
  animation-direction: alternate-reverse;
  animation-duration: 4s;
}

.bg3 {
  animation-duration: 5s;
}

.content {
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 0.25em;
  box-shadow: 0 0 0.25em rgba(0, 0, 0, 0.25);
  box-sizing: border-box;
  padding: 10vmin;
  position: absolute;
  text-align: center;
  transform: translate(-50%, -50%);
}

h1 {
  font-family: monospace;
}

@keyframes slide {
  0% {
    transform: translateX(-25%);
  }
  100% {
    transform: translateX(25%);
  }
}
</style>