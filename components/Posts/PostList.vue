<template>
  <section class="posts-list">
    <!-- <PostPreview
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      :is-admin="isAdmin"
      :title="post.title"
      :thumbnail="post.thumbnail"
      :preview-text="post.previewText"
      test="test"
    /> -->
    <PostPreview v-for="post in posts" v-bind="post" :key="post.id" />
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
    posts: {
      type: Array,
      required: true,
    },
  },
  methods: {},
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
