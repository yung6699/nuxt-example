<template>
  <div>
    <div>{{ $route.params.id }}</div>
    <div>$route.params.id</div>
  </div>
</template>

<script>
export default {
  layout: 'users',

  validate(data) {
    return /^\d+$/.test(data.params.id)
  },
}
</script>

<style scoped></style>
