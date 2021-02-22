<template>
  <form @submit.prevent="onSave">
    <AppControlInput v-model="editedPost.author">Author Name</AppControlInput>
    <AppControlInput v-model="editedPost.title">Title</AppControlInput>
    <AppControlInput v-model="editedPost.thumbnailLink"
      >Thumbnail Link</AppControlInput
    >
    <AppControlInput v-model="editedPost.content" control-type="textarea"
      >Content</AppControlInput
    >
    <AppButton type="submit">Save</AppButton>
    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel"
      >Cancel</AppButton
    >
  </form>
</template>

<script>
export default {
  name: 'AdminPostForm',
  components: {
    AppControlInput: () => import('@/components/UI/AppControlInput'),
    AppButton: () => import('@/components/UI/AppButton'),
  },

  props: {
    post: {
      type: Object,
      required: false,
    },
  },

  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : {
            author: '',
            title: '',
            thumbnailLink: '',
            content: '',
          },
    }
  },

  methods: {
    onCancel() {
      this.$router.push('/admin')
    },
    onSave() {
      console.log('onSave', this.editedPost)
    },
  },
}
</script>

<style scoped></style>
