<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the lastest tech news!</h1>
    </section>
    <PostList :posts="loadedPosts" />
    <!-- <AppControlInput @input="onInput" @focus="onFocus" @blur="onBlur" /> -->
  </div>
</template>

<script>
export default {
  components: {
    PostList: () => import('@/components/Posts/PostList'),
    // AppControlInput: () => import('@/components/UI/AppControlInput'),
  },
  asyncData(context, callback) {
    // eslint-disable-next-line nuxt/no-timing-in-fetch-data
    setTimeout(() => {
      console.log('setTimeout callback')
      callback(null, {
        loadedPosts: [
          {
            id: 1,
            title: 'First Post',
            previewText: 'This is our first post!',
            isAdmin: false,
            thumbnail:
              'http://imagescdn.gettyimagesbank.com/500/19/050/984/0/1179111980.jpg',
          },
          {
            id: 2,
            title: 'Second Post',
            previewText: 'This is our second post!',
            isAdmin: false,
            thumbnail:
              'http://imagescdn.gettyimagesbank.com/500/19/050/984/0/1179111980.jpg',
          },
        ],
      })
    }, 5000)
  },
  data() {
    return {
      loadedPosts: [],
    }
  },
  methods: {
    onInput(e) {
      console.log('input', e.target.value)
    },
    onFocus(e) {
      console.log('focus', e.target.value)
    },
    onBlur(e) {
      console.log('blur', e.target.value)
    },
  },
}
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('./assets/images/main-page-background.jpg');
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}
</style>
