<template>
  <div class="post">
    <div class="header">
      <div class="avatar">
        <a href="#">
          <img :src="avatars_link" />
        </a>
      </div>
      <div class="topname">
        <a href="#">
          <h4>Имя пользователя</h4>
        </a>
        <div class="location">
          <a href="#">Место</a>
        </div>
      </div>
    </div>
    <img :src="image_link" />
    <div class="icon">
      <a href="#">
        <img :src="icon_link1" />
      </a>
      <a href="#">
        <img :src="icon_link2" />
      </a>
      <a href="#">
        <img :src="icon_link3" />
      </a>
    </div>

    <Comment v-for="(comment, index) in comments_array" v-bind:key="index" v-bind:text="comment" />
  </div>
</template>

<script>
import Comment from "./Comment.vue";

export default {
  data: function() {
    return {};
  },
  props: [
    "image_link",
    "avatars_link",
    "icon_link1",
    "icon_link2",
    "icon_link3",
    "comments_array"
  ],
  components: {
    Comment
  }
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
}

.post {
  margin-bottom: 30px;
  border: 1px solid silver;
  background-color: white;
}
.post img {
  alt: "";
  width: 100%;
  height: 100%;
}
.header {
  display: flex;
  align-items: center;
}
.avatar {
  margin-top: 5px;
  margin-left: 10px;
}
.avatar img {
  alt: "";
  border-radius: 50px;
  border: 3px solid rgb(172, 9, 172);
  padding: 2px;
  width: 50px;
  height: 50px;
}
.topname {
  margin-left: 10px;
}
.location {
  font-size: 90%;
}
.icon {
  display: flex;
  padding-left: 15px;
  padding-bottom: 15px;
  width: 100px;
  height: 20px;
  justify-content: space-around;
}
.icon img {
  alt: "";
  padding-top: 5px;
  width: 20px;
  height: 20px;
}
</style>
