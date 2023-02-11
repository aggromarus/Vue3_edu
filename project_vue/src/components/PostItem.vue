<template>
  <div class="post">
    <div>
      <div><strong>Название поста:</strong> {{ post.title }}</div>
      <div><strong>Текст поста:</strong> {{ post.body }}</div>
    </div>
    <div class="post__btns">
      <my-button
          @click="$emit('remove', post)"
      >
        Delete post
      </my-button>
    </div>
  </div>
</template>

<script>

export default {
  name: "PostItem",
  props:{
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
.post {
  border: thick double #32a1ce;
  margin-top: 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
}
</style>