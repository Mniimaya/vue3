<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
      @input="title = $event.target.value"
      v-bind:value="title"
      class="input"
      type="text"
      placeholder="Заголовок"
    />
    <input
      @input="body = $event.target.value"
      v-bind:value="body"
      class="input"
      type="text"
      placeholder="Описание"
    />
    <button @click="createPost" class="button">Создать</button>
  </form>
</template>

<script>
export default {}
</script>

<style scoped>
.input {
  padding: 5px 10px;
  margin-top: 15px;
  width: 400px;
  display: block;
  border: 1px solid teal;
}

.button {
  margin-top: 15px;
  background-color: bisque;
  color: black;
  padding: 10px 15px;
  border: none;
  font-size: 16px;
}
</style>
