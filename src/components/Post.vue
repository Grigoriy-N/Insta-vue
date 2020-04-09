<template>
  <div style="width: 50%; margin: auto">
    <div class="grid">
      <div class="grid-item1">
        <div class="post">
          <div class="header">
            <div class="avatar">
              <a href="#"><img :src="avatar1"/></a>
            </div>
            <div class="topname">
              <a href="#"> <h4>Имя пользователя</h4></a>
              <div class="location">
                <a href="#"> Место</a>
              </div>
            </div>
          </div>
          <img :src="postimage1" />
          <div class="icon">
            <a href="#"><img :src="icon1"/></a>
            <a href="#"><img :src="icon2"/></a>
            <a href="#"><img :src="icon3"/></a>
          </div>

          <Comment
            v-for="(item, index) in comments_array"
            v-bind:key="index"
            v-bind:text="item"
          />
        </div>
        <div class="post">
          <div class="header">
            <div class="avatar">
              <a href="#"><img :src="avatar2"/></a>
            </div>
            <div class="topname">
              <a href="#"> <h4>Имя пользователя</h4></a>
              <div class="location">
                <a href="#"> Место</a>
              </div>
            </div>
          </div>
          <img :src="postimage2" />
          <div class="icon">
            <a href="#"><img :src="icon1"/></a>
            <a href="#"><img :src="icon2"/></a>
            <a href="#"><img :src="icon3"/></a>
          </div>

          <Comment
            v-for="(item, index) in comments_array"
            v-bind:key="index"
            v-bind:text="item"
          />
        </div>
      </div>
      <div class="grid-item2">
        <div class="userbar">
          <img :src="avatar3" />
          <h4 style="font-size: 90%; margin-left: 10px">Имя пользователя</h4>
        </div>
        <div class="mainstories">
          <p style="padding-left: 10px; padding-top: 5px">Истории</p>
          <div class="stories">
            <img :src="avatar4" />
            <div>
              <h4 style="font-size: 90%;margin-left: 10px">
                Имя пользователя
              </h4>
              <p style="color: gray;font-size: 85%; margin-left: 10px">
                10 часов назад
              </p>
            </div>
          </div>
          <div class="stories">
            <img :src="avatar5" />
            <div>
              <h4 style="font-size: 90%;margin-left: 10px">
                Имя пользователя
              </h4>
              <p style="color: gray;font-size: 85%; margin-left: 10px">
                15 часов назад
              </p>
            </div>
          </div>
        </div>
        <div class="mainrecommendation">
          <p style="padding-left: 10px; padding-top: 5px">Рекомендации для вас</p>
          <div class="recommendation">
            <img :src="avatar4" />
            <div>
              <h4 style="font-size: 90%;margin-left: 10px">
                Имя пользователя
              </h4>
              <p style="color: gray;font-size: 85%; margin-left: 10px">
                Рекомендации
              </p>
            </div>
          </div>
          <div class="recommendation">
            <img :src="avatar5" />
            <div>
              <h4 style="font-size: 90%;margin-left: 10px">
                Имя пользователя
              </h4>
              <p style="color: gray;font-size: 85%; margin-left: 10px">
                Рекомендации
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Comment from "./Comment";
export default {
  data: function() {
    return {
      comments: [""],
      avatar1: "https://avatarfiles.alphacoders.com/150/thumb-150628.jpg",
      avatar2: "https://avatarfiles.alphacoders.com/186/thumb-186110.jpg",
      avatar3: "https://avatarfiles.alphacoders.com/138/thumb-138931.jpg",
      avatar4: "https://avatarfiles.alphacoders.com/618/thumb-61836.jpg",
      avatar5: "https://avatarfiles.alphacoders.com/181/thumb-181745.jpg",
      postimage1:
        "https://s.zefirka.net/images/2017-05-29/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro-2.jpg",
      postimage2:
        "https://s.zefirka.net/images/2017-05-29/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro/krasivye-gorodskie-pejzazhi-iz-instagram-vincent-cogliandro-7.jpg",
      icon1: "https://img.icons8.com/ios/100/000000/like.png",
      icon2: "https://img.icons8.com/ios/50/000000/comments.png",
      icon3: "https://img.icons8.com/metro/52/000000/paper-plane.png"
    };
  },
  props: ["image_link", "comments_array"],
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
.grid {
  display: grid;
  grid-template-areas: "a1 a2";
  grid-template-columns: 2fr 1fr;
  justify-content: center;
  grid-gap: 2em;
  background: rgb(247, 244, 244);
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
.userbar {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}
.userbar img {
  alt: "";
  border-radius: 50px;
  width: 60px;
  height: 60px;
}
.mainstories {
  border: 1px solid silver;
  margin-bottom: 30px;
  background: white;
}
.stories {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}
.stories img {
  alt: "";
  border-radius: 50px;
  border: 3px solid rgb(172, 9, 172);
  padding: 2px;
  width: 50px;
  height: 50px;
  margin-top: 5px;
  margin-left: 10px;
}
.mainrecommendation {
  border: 1px solid silver;
  margin-bottom: 30px;
  background: white;
}
.recommendation {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}
.recommendation img {
  alt: "";
  border-radius: 50px;
  padding: 2px;
  width: 50px;
  height: 50px;
  margin-top: 5px;
  margin-left: 10px;
}
</style>
