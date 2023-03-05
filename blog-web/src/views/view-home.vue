<template>
  <div class="view-home">
    <blue-back></blue-back>
    <div class="show">
      <div class="container">
        <blue-box :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :box-type="boxType" :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :box-type="boxType" :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :box-type="boxType" :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :description="description" :img-path="imgPath" :title="title"></blue-box>
        <blue-box :box-type="boxType" :description="description" :img-path="imgPath" :title="title"></blue-box>
      </div>
      <div class="container-side">
        <blue-box name="blue smile" box-type="blank"></blue-box>
      </div>
    </div>
  </div>
</template>

<script>
import BlueBack from "@/components/blue-back";
import BlueBox from "@/components/blue-box";

export default {
  name: "view-home",
  components: {BlueBox, BlueBack},
  data() {
    return {
      boxType: 'right',
      title: '测试组件',
      description: '这是一个测试的组件,这是一个测试的组件,这是一个测试的组件,这是一个测试的组件,这是一个测试的组件,这是一个测试的组件,这是一个测试的组件,这是一个测试的组件',
      imgPath: 'http://www.forclementine.com:8088/resource/back.png'
    }
  }
}
</script>

<style scoped>
.show{
  display: flex;
  overflow: hidden;
  margin: 0 auto;
  /*border: #5f5f5f solid 2px;*/
  width: 1280px;
}
.container {
  width: 892px;
}

.container-side {
  width: 280px;
  height: 360px;
  /*border: #5f5f5f solid 2px;*/
}
</style>