<template>
  <div class="blue-back">
    <img src="../static/back.png" :height="height" alt="">
  </div>
</template>

<script>
export default {
  name: "blue-back",
  data(){
    return{
      height: window.innerHeight
    }
  }
}
</script>

<style scoped>
  /*.blue-back{*/
  /*  position: absolute;*/
  /*  top: 0;*/
  /*}*/
  .blue-back img{
    width: 100%;
  }
</style>