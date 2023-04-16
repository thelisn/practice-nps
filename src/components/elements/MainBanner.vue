<template>
  <div class="wrap">
  <div class="mainbanner" v-for="item in bannerImg" :key="item">
    <a href="#">
    <img :src="item.url" alt="배너이미지">
    </a>
  </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      bannerImg: [
        {url: require("../../assets/images/banner1.png")},
        {url: require("../../assets/images/banner2.png")},
        {url: require("../../assets/images/banner3.png")},
        {url: require("../../assets/images/banner4.png")}
      ]
    }
  }
}

</script>

<style scoped lang="scss">

.wrap {
  width: 1100px;
  margin: 0 auto;
.mainbanner {
  background: #ccc;
  width: 580px;
  height: 350px;
  // display: inline-block;
  position: absolute;
  margin-top: 30px;
  border-radius: 30px;
  overflow: hidden;
  // box-shadow: 0px 0px 8px #ccc;

  img {
    height: 350px;
    margin-left: -30px;
  }
}
}
</style>