<template>
  <div class="admin-page">
    <section class="new-post">
      <AppButton @click.native="$router.push('/admin/new-post')"
        >Create Post</AppButton
      >
    </section>
    <section class="existing-posts">
      <h1>Existing Posts</h1>
      <PostList />
    </section>
  </div>
</template>

<script>
export default {
  components: {
    PostList: () => import('@/components/Posts/PostList'),
    AppButton: () => import('@/components/Posts/PostList'),
  },
}
</script>

<style scoped>
.admin-page {
  padding: 20px;
}

.new-post {
  text-align: center;
  border-bottom: 2px solid #ccc;
  padding-bottom: 10px;
}

.existing-posts h1 {
  text-align: center;
}
</style>
