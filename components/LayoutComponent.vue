<template>
  <div class="">
    <div class="navbar">
      <div class="navbar--container">
        <h4>Container</h4>
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

<style scoped>
.navbar {
  @apply bg-gray-50 top-0 absolute w-full h-12
    filter drop-shadow-sm;
}
</style>

