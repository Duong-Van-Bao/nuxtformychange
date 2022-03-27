<template>
  <div>
    <h1>Your deck {{ $route.params.id }} is active.</h1>
  </div>
</template>

<script>
export default {
  validate ({ params }) {
    return /^[0-9]{9,12}$/.test(params.id)
  }
}
</script>

<style lang="scss" scoped>
</style>
