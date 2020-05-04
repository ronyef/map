<template>
  <v-container>
    <h1>{{blogPost.title}}</h1>
    <div v-html="$md.render(blogPost.body)"/>
  </v-container>
</template>

<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { blogPost: payload };
    else
      return {
        blogPost: await require(`~/assets/content/blog/${params.blog}.json`)
      };
  }
};
</script>

<style>
</style>
