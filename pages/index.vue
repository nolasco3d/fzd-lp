<template>
  <LayoutComponent>
    <template #content>
      <BannerHero />
      <div class="product--grid">
        <template v-for="(product, index) in products">
          <div :key="`product-${index}`" class="product--card">
            <h4>{{ product.name }}</h4>
            <p>{{ product.desc }}</p>
            <span>{{ product.price }}</span>
            <button>Click</button>
          </div>
        </template>
      </div>
    </template>
  </LayoutComponent>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      products: [
        {
          name: 'Prod 1',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repellendus non vitae nulla?',
          price: 12392,
          img: 'none',
        },
        {
          name: 'Prod 1',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repellendus non vitae nulla?',
          price: 12392,
          img: 'none',
        },
        {
          name: 'Prod 1',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repellendus non vitae nulla?',
          price: 12392,
          img: 'none',
        },
        {
          name: 'Prod 1',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Repellendus non vitae nulla?',
          price: 12392,
          img: 'none',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.product {
  &--grid {
    @apply border border-gray-200 grid grid-cols-3 gap-5 p-5;
    margin-top: -120px;
    padding-bottom: -120px;
  }
  &--card {
    @apply
      border border-gray-200 bg-gray-100 text-gray-600
      rounded rounded-lg
      p-3;
  }
}
</style>
