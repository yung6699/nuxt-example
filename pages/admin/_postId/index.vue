<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
export default {
  components: {
    AdminPostForm: () => import('@/components/Admin/AdminPostForm'),
  },
  data() {
    return {
      loadedPost: {
        author: 'Maximilian',
        title: 'My awesome Post',
        content: 'Super amazing, thanks for that!',
        thumbnailLink:
          'http://imagescdn.gettyimagesbank.com/500/19/050/984/0/1179111980.jpg',
      },
    }
  },
}
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
