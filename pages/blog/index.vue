<template>
  <div>
    <ul>
      <nuxt-link v-for="post in blogPosts" :to="{ path: `/blog/${post.slug}` }" :key="post.slug">{{post.title}}</nuxt-link>
    </ul>
  </div>
</template>
<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    },
  },
};
</script>
