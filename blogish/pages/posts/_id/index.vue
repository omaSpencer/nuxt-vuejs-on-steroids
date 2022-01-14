<template>
  <div class="single-post-page">
    <section class="post">
      <h1 class="post-title">{{ post.title }}</h1>
      <div class="post-details">
        <div class="post-detail">
          last updated: {{ post.updatedAt.toLocaleTimeString() }}
        </div>
        <div class="post-detail">written by: {{ post.author }}</div>
      </div>
      <p class="post-content">{{ post.content }}</p>
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
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        post: {
          id: '1',
          title: `First ${context.params.id}`,
          lead: 'Lead',
          author: 'Spencer',
          updatedAt: new Date(),
          content:
            'Laboris magna aute qui eiusmod cillum minim occaecat non irure id consectetur. Cupidatat eu fugiat consequat dolor do irure ullamco laborum ad minim esse esse. Veniam velit in exercitation id tempor. Pariatur sit id ad ipsum. Irure minim aute quis cupidatat fugiat laborum est voluptate magna ut aute. Magna in consequat velit ex culpa duis fugiat nostrud esse elit ut.',
          thumbnail:
            'https://images.unsplash.com/photo-1642006255340-61a8d8eb7c95?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80',
        },
      })
    }, 1000)
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
