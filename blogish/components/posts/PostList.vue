<template>
  <section class="posts-list">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :is-admin="isAdmin"
      :title="post.title"
      :lead="post.lead"
      :thumbnail="post.thumbnail"
    />
  </section>
</template>

<script>
import PostPreview from '@/components/posts/PostPreview'

export default {
  name: 'PostList',
  components: { PostPreview },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
      required: false,
    },
    posts: {
      type: Array,
      required: true,
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
  gap: 30px;
}
</style>
