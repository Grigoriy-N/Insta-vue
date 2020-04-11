<template>
  <div>
    <div class="userbar">
      <img :src="avatars.ava1" />
      <h4 style="font-size: 90%; margin-left: 10px">Имя пользователя</h4>
    </div>
    <div class="mainstories">
      <p class="heading">Истории</p>
      <div class="stories">
        <img :src="avatars.ava2" />
        <div>
          <h4 class="username">Имя пользователя</h4>
          <p class="signature">10 часов назад</p>
        </div>
      </div>
      <div class="stories">
        <img :src="avatars.ava3" />
        <div>
          <h4 class="username">Имя пользователя</h4>
          <p class="signature">15 часов назад</p>
        </div>
      </div>
    </div>
    <div class="mainrecommendation">
      <p class="heading">Рекомендации для вас</p>
      <div class="recommendation">
        <img :src="avatars.ava4" />
        <div>
          <h4 class="username">Имя пользователя</h4>
          <p class="signature">Рекомендации</p>
        </div>
      </div>
      <div class="recommendation">
        <img :src="avatars.ava5" />
        <div>
          <h4 class="username">Имя пользователя</h4>
          <p class="signature">Рекомендации</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      avatars: {
        ava1: "https://avatarfiles.alphacoders.com/138/thumb-138931.jpg",
        ava2: "https://avatarfiles.alphacoders.com/618/thumb-61836.jpg",
        ava3: "https://avatarfiles.alphacoders.com/181/thumb-181745.jpg",
        ava4: "https://avatarfiles.alphacoders.com/160/thumb-160213.jpg",
        ava5: "https://avatarfiles.alphacoders.com/168/thumb-168689.jpg"
      }
    };
  }
};
</script>



<style scoped>
* {
  padding: 0;
  margin: 0;
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
.heading {
  padding-left: 10px;
  padding-top: 5px;
}
.username {
  font-size: 90%;
  margin-left: 10px;
}
.signature {
  color: gray;
  font-size: 85%;
  margin-left: 10px;
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