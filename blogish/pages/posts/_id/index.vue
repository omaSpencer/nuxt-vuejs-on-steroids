<template>
  <div class="single-post-page">
    <section class="post">
      <h1 class="post-title">{{ post.title }}</h1>
      <div class="post-details">
        <div class="post-detail">
          last updated: {{ new Date(post.updatedAt).toLocaleTimeString() }}
        </div>
        <div class="post-detail">written by: Spencer</div>
      </div>
      <p class="post-content">{{ post.description }}</p>
    </section>
    <section class="post-feedback">
      <p>
        let me know what you think, send a mail to
        <a href="mailto:" target="_blank" rel="noopener noreferrer"
          >feedback@example.com</a
        >
      </p>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ params, $http }) {
    const post = await $http.$get(`https://api.nuxtjs.dev/posts/${params.id}`)

    return { post }
  },
}
</script>

<style scoped>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}
.post {
  width: 100%;
}
@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}
.post-title {
  margin: 0;
}
.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}
.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}
.post-feedback a {
  color: red;
  text-decoration: none;
}
.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}
</style>
