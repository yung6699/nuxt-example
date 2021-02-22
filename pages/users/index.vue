<template>
  <div>
    <p>Please enter default Component</p>
  </div>
</template>

<script>
export default {
  layout: 'users',
  data() {
    return {
      userId: '',
    }
  },

  methods: {
    onLoadUser() {
      this.$router.push(`/users/${this.userId}`)
    },
  },
}
</script>

<style scoped></style>
