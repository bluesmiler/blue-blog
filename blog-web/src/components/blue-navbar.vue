<template>
  <div class="blue-navbar" :style="{'box-shadow':shadow,'top': top,'transition':transition,'background':background}">
    <ul>
      <li :style="{'color': fontColor}">首页</li>
      <li :style="{'color': fontColor}">发现</li>
      <li :style="{'color': fontColor}">娱乐</li>
      <li :style="{'color': fontColor}">关于</li>
      <li :style="{'color': fontColor}">留言</li>
      <li :style="{'color': fontColor}">登录</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "blue-navbar",
  data() {
    return {
      scrollPosition: 0,
      top: '',
      background: '',
      transition: '',
      fontColor: '',
      shadow: 'none'
    }
  },
  methods: {
    handleScroll() {
      const scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
      const scroll = scrollTop - this.scrollPosition;
      this.scrollPosition = scrollTop
      if (scroll > 0) {
        this.hiddenNavbar()
      } else {
        this.showNavbar()
      }
    },
    hiddenNavbar() {
      this.top = '-60px'
      this.transition = 'all 0.8s'
      this.background = 'rgba(255,255,255,0.85)'
      this.fontColor = '#dfdada'
      this.shadow = '#948d8d 0 0 10px'
    },
    showNavbar() {
      this.top = '0'
      this.transition = 'all 0.8s'
      this.background = 'rgba(255,255,255,0.85)'
      this.fontColor = '#1c1c1c'
      if (this.scrollPosition < 200) {
        this.background = 'rgba(255,255,255,0)'
        this.shadow = 'none'
        this.transition = 'all 0.5s'
        this.fontColor = '#dfdada'
      }
    }
  },
  mounted() {
    //监听滚轮移动
    window.addEventListener('scroll', this.handleScroll, true)
  },
}
</script>

<style scoped>
.blue-navbar {
  width: 100%;
  box-shadow: #948d8d 0 0 10px;
  /*position: fixed;*/
  /*top: 0;*/
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  /*overflow: hidden;*/
  /*background-color: #333;*/
}

li {
  float: left;
  display: block;
  text-align: center;
  padding: 20px 16px;
  text-decoration: none;
  transition: color 0.6s;
  color: #eff8f5;
}

/* 当鼠标悬停时把链接颜色更改为 #111（黑色） */
li:hover {
  color: rgba(68, 180, 239, 0.81);
  cursor: pointer;
}
</style>