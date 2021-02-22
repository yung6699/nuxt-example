<template>
  <section class="posts-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      title="Hello There"
      thumbnail="http://imagescdn.gettyimagesbank.com/500/19/050/984/0/1179111980.jpg"
      preview-text="Lorem ipsum Lorem ipsum Lorem ipsum"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      title="Hello There 02"
      thumbnail="http://imagescdn.gettyimagesbank.com/500/19/050/984/0/1179111980.jpg"
      preview-text="Lorem ipsum Lorem ipsum Lorem ipsum"
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      title="Hello There 03"
      thumbnail="http://imagescdn.gettyimagesbank.com/500/19/050/984/0/1179111980.jpg"
      preview-text="Lorem ipsum Lorem ipsum Lorem ipsum"
    />
  </section>
</template>

<script>
export default {
  components: {
    PostPreview: () => import('@/components/Posts/PostPreview'),
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: true,
    },
  },
}
</script>

<style scoped>
.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
