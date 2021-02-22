<template>
  <div class="posts-page">
    <PostList />
  </div>
</template>

<script>
export default {
  name: 'Index',
  components: {
    PostList: () => import('@/components/Posts/PostList'),
  },
}
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
