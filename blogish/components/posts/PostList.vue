<template>
  <section class="posts-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      title="Title"
      lead="Lorem ipsum dolor sit amet, consectetur adipiscing el"
      thumbnail="https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      title="Title"
      lead="Lorem ipsum dolor sit amet, consectetur adipiscing el"
      thumbnail="https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      title="Title"
      lead="Lorem ipsum dolor sit amet, consectetur adipiscing el"
      thumbnail="https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
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
