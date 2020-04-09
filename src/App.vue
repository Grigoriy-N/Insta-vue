<template>
  <div id="app">
    <Header />
    <Post
      v-for="(item, index) in posts"
      v-bind:key="index"
      v-bind:comments_array="item.comments"
    />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Post from "./components/Post.vue";

export default {
  name: "app",
  data() {
    return {
      posts: [
        {
          comments: [
            "Lorem, ipsum dolor sit amet consectetur.",
            "Lorem ipsum dolor sit amet consectetur adipisicing elit."
          ]
        }
      ]
    };
  },
  components: {
    Header,
    Post
  }
};
</script>

<style></style>
