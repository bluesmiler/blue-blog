<template>
  <div class="blue-box" :name="name" :boxType="boxType" :description="description" :imgPath="imgPath" :title="title" :profile="profile">
    <div class="blue-box-left" v-if="boxType===undefined || boxType ==='left'">
      <div class="img-show">
        <img :src="imgPath" alt="">
      </div>
      <div>
        <div class="title">{{ title }}</div>
        <div class="blue-box-left-p">
          <p>{{ description }}</p>
        </div>
      </div>

    </div>
    <div class="blue-box-left" v-if="boxType==='right'">
      <div>
        <div class="title">{{ title }}</div>
        <div class="blue-box-left-p">
          <p>{{ description }}</p>
        </div>
      </div>
      <div class="img-show">
        <img :src="imgPath" alt="">
      </div>
    </div>
    <div class="blue-box-blank" v-if="boxType==='blank'">
      <div>
        <img :src="imgPath?undefined:'http://www.forclementine.com:8088/resource/author.ico'" alt="">
      </div>
      <div>
        <h1>{{ name }}</h1>
      </div>
      <div>
        <p>{{ profile?undefined:'这个家伙很懒,什么都没写' }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "blue-box",
  props: {
    boxType: String,
    description: String,
    imgPath: String,
    title: String,
    name: String,
    profile: String
  },
}
</script>

<style scoped>
.img-show {
  width: 380px;
  height: 300px;
  margin: 0;
  overflow: hidden;
  transition: 0.6s;
}

.img-show img {
  width: 380px;
  height: 300px;
  margin: 0;
  transition: 0.6s;
}

img:hover {
  cursor: pointer;
}

.blue-box-left-p {
  width: 400px;
  /*border: #5f5f5f solid 2px;*/
  margin: 16px 40px;
  text-indent: 2em;
}

.title {
  text-align: center;
  font-size: 22px;
  font-weight: bold;
}

.title:hover {
  cursor: pointer;
  color: #825dae;
  transition: 0.5s;
}

.blue-box-left {
  display: flex;
  width: 860px;
  height: 280px;
  border-radius: 12px;
  align-items: center;
  justify-content: space-between;
  overflow: hidden;
  margin: 40px;
  background: white;
  box-shadow: #d0cbcb 0 0 10px;
  transition: 0.4s;
}
.blue-box-left:hover {
  box-shadow: #a09a9a 0 0 40px;
  transition: 0.4s;
}

.blue-box-blank {
  display: flex;
  width: 280px;
  height: 360px;
  margin: 40px;
  /*border: #5f5f5f solid 2px;*/
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background: white;
  border-radius: 12px;
  box-shadow: #d0cbcb 0 0 10px;
  transition: 0.4s;
}
.blue-box-blank:hover {
  box-shadow: #a09a9a 0 0 40px;
  transition: 0.4s;
}

.blue-box-blank img {
  width: 140px;
  height: 140px;
}

.blue-box-left:hover img {
  transform: scale(1.1);
  transition: 0.6s;
}
</style>