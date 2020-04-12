<template>
  <div id="app">
    <Header />
    <div class="grid">
      <div class="grid-item1">
        <Post
          v-for="(item, index) in posts"
          :key="index"
          :image_link="item.image_url"
          :avatars_link="item.avatars_url"
          :icon_link1="item.icons_url1"
          :icon_link2="item.icons_url2"
          :icon_link3="item.icons_url3"
          :comments_array="item.comments"
        />
      </div>

      <Stories class="grid-item2"></Stories>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Post from "./components/Post.vue";
import Stories from "./components/Stories.vue";

export default {
  name: "app",
  data() {
    return {
      posts: [
        {
          image_url: [
            "https://s.zefirka.net/images/2017-05-29/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro-2.jpg"
          ],
          avatars_url: [
            "https://avatarfiles.alphacoders.com/150/thumb-150628.jpg"
          ],
          icons_url1: ["https://img.icons8.com/ios/100/000000/like.png"],
          icons_url2: ["https://img.icons8.com/ios/50/000000/comments.png"],
          icons_url3: [
            "https://img.icons8.com/metro/52/000000/paper-plane.png"
          ],
          comments: ["Коммент 1", "Коммент 2"]
        },
        {
          image_url: [
            "https://s.zefirka.net/images/2017-05-29/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro-7.jpg"
          ],
          avatars_url: [
            "https://avatarfiles.alphacoders.com/186/thumb-186110.jpg"
          ],
          icons_url1: ["https://img.icons8.com/ios/100/000000/like.png"],
          icons_url2: ["https://img.icons8.com/ios/50/000000/comments.png"],
          icons_url3: [
            "https://img.icons8.com/metro/52/000000/paper-plane.png"
          ],
          comments: ["Коммент 1", "Коммент 2"]
        }
      ]
    };
  },
  components: {
    Header,
    Post,
    Stories
  }
};
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-areas: "a1 a2";
  grid-template-columns: 2fr 1fr;
  justify-content: center;
  grid-gap: 2em;
  background: rgb(247, 244, 244);
  width: 50%;
  margin: auto;
  
}

.grid-item1 {
  grid-area: a1;
}
.grid-item2 {
  align-self: start;
  grid-area: a2;
  position: sticky;
  top: 80px;
}
</style>
