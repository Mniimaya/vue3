<template>
  <ul>
    <li class="post" v-for="post in posts" :key="post.id">
      <div>
        <p>
          Название:
          <span
            ><strong>{{ post.title }}</strong></span
          >
        </p>
        <p>
          Описание:
          <span
            ><strong>{{ post.body }}</strong></span
          >
        </p>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array
    }
  }
}
</script>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}
</style>
