<template>
  <LayoutComponent>
    <template #content>
      <BannerHero />
      <div class="step--grid">
        <template v-for="(step, index) in steps">
          <div :key="`step-${index}`" class="step--card">
            <i class="flex-1" :class="step.icon">i</i>
            <div class="step--card--textbox">
              <h4>{{ step.name }}</h4>
              <p>{{ step.description }}</p>
            </div>
          </div>
        </template>
      </div>

      <!-- <div class="step--grid">
        <template v-for="(step, index) in steps">
          <div :key="`step-${index}`" class="step--card">
            <h4>{{ step.name }}</h4>
            <p>{{ step.desc }}</p>
            <span>{{ step.price }}</span>
            <button>Click</button>
          </div>
        </template>
      </div> -->
      <div class="">

      </div>
    </template>
  </LayoutComponent>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      steps: [
        {
          icon: 'check',
          name: 'Step name one',
          description: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          icon: 'check',
          name: 'Step name one',
          description: 'Lorem ipsum dolor sit amet consectetur.'
        },
        {
          icon: 'check',
          name: 'Step name one',
          description: 'Lorem ipsum dolor sit amet consectetur.'
        }
      ],
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

.step {
  &--grid {
    @apply grid grid-cols-3 gap-5 p-5;
  }

  &--card {
    @apply border border-gray-200 bg-gray-100
      text-gray-600
      rounded rounded-lg
      flex
      p-3;

    &--textbox {
    @apply w-3/4;
    }
  }
}
</style>
