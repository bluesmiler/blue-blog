<template>
  <blue-navbar></blue-navbar>
  <view-home></view-home>
</template>

<script>

import BlueNavbar from "@/components/blue-navbar";
import ViewHome from "@/views/view-home";

export default {
  name: 'App',
  components: {ViewHome, BlueNavbar},
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  background: linear-gradient(to right, #f6eee8, #f1d6f0, #eceff8, #e3fbf4);
  font-family:Arial, Helvetica, sans-serif;
  font-size: 15px;
  color:#5f5f5f;
}
.blue-navbar{
  position: fixed;
  z-index: 2;
}
::-webkit-scrollbar {
  list-style: none;
  width: 8px;
  height: 50px;
}
/* 滚动槽 */
::-webkit-scrollbar-track {
  /*border-radius: 10px;*/
}

/* 滚动条滑块 */
::-webkit-scrollbar-thumb {
  border-radius: 10px;
  background-color: rgba(131, 182, 241, 0.69);
  -webkit-transition: 0.3s background-color;
  transition: 0.3s background-color;
}

</style>
