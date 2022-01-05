<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/admin/AdminPostForm'

export default {
  layout: 'admin',
  components: { AdminPostForm },
  data() {
    return {
      loadedPost: {
        author: 'Spencer',
        title: 'Post',
        content:
          'Qui officia aliqua anim Lorem officia laboris cupidatat laborum laborum ea ea voluptate voluptate esse.',
        thumbnailLink:
          'https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80',
      },
    }
  },
}
</script>
