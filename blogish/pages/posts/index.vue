<template>
  <div class="posts-page">
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from '@/components/posts/PostList'

export default {
  components: {
    PostList,
  },
  async asyncData(context, callback) {
    try {
      const data = await new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            posts: [
              {
                id: '1',
                title: 'First',
                lead: 'Lead',
                thumbnail:
                  'https://images.unsplash.com/photo-1642006255340-61a8d8eb7c95?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80',
              },
            ],
          })
        }, 1500)
      })
      return data
    } catch (e) {
      context.error(e)
    }
  },
}
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
