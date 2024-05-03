<template>
  <div class="wrapper">
    <post-form />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostList from './components/PostList.vue'
import PostForm from './components/PostForm.vue'
export default {
  components: {
    PostList,
    PostForm
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'JavaScript 1', body: 'Рыба текст' },
        { id: 2, title: 'JavaScript 2', body: 'Рыба текст' },
        { id: 3, title: 'JavaScript 3', body: 'Рыба текст' },
        { id: 4, title: 'JavaScript 4', body: 'Рыба текст' }
      ],
      title: '',
      body: ''
    }
  },
  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body
      }

      this.posts.push(newPost)
      this.title = ''
      this.body = ''
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.wrapper {
  padding: 30px 20px;
}
</style>
