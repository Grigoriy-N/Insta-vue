<template>
  <div class="parent1">
    <div style="width: 50%; margin: auto">
      <div class="parent2">
        <h2>
          <em>
            <a href="index.html">Instaclone</a>
          </em>
        </h2>

        <div style="padding:5px">
          <input placeholder="Поиск" type="search" />
        </div>
        <div>
          <a href="index.html">
            <img
              src="https://img.icons8.com/material-rounded/96/000000/home-page.png"
              alt
              width="22"
              height="22"
              title="main"
            />
          </a>

          <a href="explore.html">
            <img
              src="https://img.icons8.com/metro/52/000000/compass.png"
              alt
              width="20"
              height="20"
              title="explore"
            />
          </a>

          <a href="#">
            <img
              src="https://img.icons8.com/ios/100/000000/like.png"
              alt
              width="22"
              height="22"
              title="accountactivity"
            />
          </a>

          <a href="userprofile.html">
            <img
              src="https://avatarfiles.alphacoders.com/138/thumb-138931.jpg"
              alt
              style="border-radius: 20px"
              width="22"
              height="22"
              title="userprofile"
            />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  padding: 0;
  margin: 0;
}
.parent1 {
  background-color: white;
  position: sticky;
  top: 0;
  border-bottom: 1px solid gray;
  margin-bottom: 30px;
}
.parent2 {
  padding-top: 10px;
  padding-bottom: 10px;
  background-color: white;
  display: flex;
  justify-content: space-between;
}
</style>


