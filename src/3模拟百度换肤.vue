<template>
  <div class="container">
    <div class="imglist">
      <h3>图片列表区</h3>
      <img src="./assets/01.jpg" alt="" @mouseover="fn(0)" @click="btn(0)"/>
      <img src="./assets/02.jpg" alt="" @mouseover="fn(1)" @click="btn(1)"/>
      <img src="./assets/03.jpg" alt="" @mouseover="fn(2)" @click="btn(2)"/>
    </div>
    <div class="show">
      <h3>图片预览区</h3>
      <img :src="imgUrl" alt="" style="width: 600px; height: auto" />
    </div>
    <div></div>
  </div>
</template>

<script>
import img1 from './assets/01.jpg'
import img2 from './assets/02.jpg'
import img3 from './assets/03.jpg'
export default {
  name: 'App',
  data() {
    return {
      imgUrl: img1,
    }
  },
  methods: {
    fn(val) {
      return (this.imgUrl = [img1, img2, img3][val])
    },
    btn(val){
      return alert(`图片是：第${val+1}张，地址是：${[img1, img2, img3][val]}`)
    }
  },
}
</script>

<style scoped>
.container {
  display: flex;
}
.imglist {
  border: 2px solid red;
}
.imglist img {
  width: 200px;
  height: auto;
}
.show {
  border: 2px solid red;
  margin-right: 20px;
}
</style>
