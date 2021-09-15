<template>
  <div>
    <row>
      <div class="hero">
        <h1>Create an online store as easy as 1, 2, 3</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipiscing elit aliquam lorem
          amet eget in netus laoreet elementum nulla dictum aam odio varius et
          purus.
        </p>
      </div>
    </row>
    <row>
      <div class="flex items-center justify-center">
        <div>
          <img
            src="@/assets/app_layout_2.svg"
            class="app-layout-2 animate__animated animate__slideInLeft"
          />
        </div>
        <div>
          <img
            src="@/assets/app_layout_1.svg"
            class="app-layout animate__animated animate__fadeInUp"
          />
        </div>
        <div>
          <img
            src="@/assets/app_layout_3.svg"
            class="animate__animated animate__slideInRight"
          />
        </div>
      </div>
    </row>
  </div>
</template>

<style lang="scss" scoped>
.hero {
  max-width: 760px;
  overflow: hidden;
  @apply text-center mx-auto mb-16;
  h1 {
    @apply text-blue-900 font-bold;
  }
  p {
    @apply text-xl text-gray-400 mt-8;
  }
}
</style>