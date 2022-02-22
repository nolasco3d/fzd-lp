<template>
  <div class="">
    <div class="navbar">
      <div class="navbar--container">
        <div class="navbar--logo">
          <!-- <img src="" alt=""> -->
        </div>
        <div class="navbar--menus">
          <div class="links"></div>
          <div class="social-media"></div>
        </div>
      </div>
    </div>
    <slot name="content" />
  </div>
</template>

<script>
export default {
  name: 'LayoutComponent'
}
</script>

<style lang="scss" scoped>
.navbar {
  @apply bg-gray-50 top-0 absolute w-full h-12
    filter drop-shadow-sm;

  &--container {
    @apply container mx-auto h-full border border-black flex;
  }
  &--logo {
    @apply border border-blue-300 h-full w-12;
  }
  &--menus {
    @apply border border-green-300 w-full;
  }
}
</style>

