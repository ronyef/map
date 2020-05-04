<template>
  <div>
    <v-row class="red py-12 px-6">
      <v-col class="pa-4">
        <v-img
          src="https://1.bp.blogspot.com/-pwRMmhgbkyY/Ucg3Mcf9coI/AAAAAAAAAhs/-8tdBgY5yKw/s1600/blogger-logo-square-webtreatsetc.png"
          max-height="300"
          contain
        ></v-img>
      </v-col>
      <v-col class="white--text pa-4">
        <h1 class="display-3">Technology</h1>
        <p class="display-4 yellow--text">BLOG</p>
        <v-btn color="black" dark large>View Projects</v-btn>
      </v-col>
    </v-row>
    <v-container class="my-10">
      <h1>Blog Page</h1>
      <p v-for="post in blogPosts" :key="post.slug">{{post.slug}}</p>
    </v-container>
  </div>
</template>

<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    }
  }
};
</script>

<style>
</style>

