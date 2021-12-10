<template>
  <section class="container">
    <nuxt-link to="/users">Users</nuxt-link>
    <button @click="$router.push('/products')">Load Products</button>
  </section>
</template>

<script>
export default {}
</script>
