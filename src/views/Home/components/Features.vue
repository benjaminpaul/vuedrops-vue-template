<template>
  <div class="features">
    <h3>Everything you need to start, scale<br />and operate your store</h3>
    <div class="flex items-center justify-center">
      <div class="feature flex flex-col items-center justify-center">
        <img src="@/assets/online_store.svg" />
        <h4>Online store</h4>
        <p>
          Lorem ipsum dolor sit amet consectetur adipiscing elit praesent mi
          magna.
        </p>
      </div>
      <div class="feature flex flex-col items-center justify-center">
        <img src="@/assets/inventory_management.svg" />
        <h4>Inventory management</h4>
        <p>
          Lorem ipsum dolor sit amet consectetur adipiscing elit praesent mi
          magna.
        </p>
      </div>
      <div class="feature flex flex-col items-center justify-center">
        <img src="@/assets/point_of_sale.svg" />
        <h4>Point of sale</h4>
        <p>
          Lorem ipsum dolor sit amet consectetur adipiscing elit praesent mi
          magna.
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.features {
  @apply text-center container mx-auto p-16;
  .feature {
    max-width: 300px;
    @apply m-4;
    img {
      @apply m-8;
    }
    h4 {
      @apply text-center;
    }
    p {
      @apply text-gray-400 mt-4;
    }
  }
}
</style>