<template>
  <div class="wrap">
    <a href="#">
      <div class="mainbanner" v-for="item in banner" :key="item">
        <!-- <img :src="item.url" alt="배너이미지"> -->
        <p class="title" v-html="item.title"></p>
        <p class="desc" v-html="item.desc"></p>
        <div class="go_btn">{{ item.go }}</div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      banner: [
        {
          title: '2023년 국민연금<br>5.1% 더 드립니다!',
          desc: '국민여러분의 더욱 든든한 노후를 위하여!<br>2022년에는 2.5% 인상',
          go: '자세히 보기 >'
        },
        {
          title: '제5차 재정계산',
          desc: '국민연금기금의 지속 가능성과 안정성 확보를 위한<br>국민연금 재정계산이 2023년 시행됩니다.',
          go: '자세히 보기 >'
        },
        {
          title: '국민연금 지역가입자<br>보험료 지원제도',
          desc: '든든한 노후를 위해 보험료 납부, 다시 시작하세요!<br>국가가 보험료의 최대 50%(월 4만 5천원까지)를 12개월까지 지원합니다.',
          go: '자세히 보기 >'
        },
        {
          title: '홈페이지에서<br>국민연금 청구 방법',
          desc: '홈페이지에서 국민연금, 노령연금 청구하는 방법을<br>영상으로 자세히 알려주고 있습니다.<br>홈페이지에서 연금 청구방법을 자세히 알아보세요.',
          go: '영상으로 보기 >'
        }

      ]
      // bannerImg: [
      //   {url: require("../../assets/images/banner1.png")},
      //   {url: require("../../assets/images/banner2.png")},
      //   {url: require("../../assets/images/banner3.png")},
      //   {url: require("../../assets/images/banner4.png")}
      // ]
    }
  }
}

</script>

<style scoped lang="scss">
.wrap {
  width: 1100px;
  margin: 0 auto;
  
  .mainbanner {
    position: absolute;
    width: 580px;
    height: 350px;
    margin-top: 30px;
    border-radius: 30px;
    background: #ccc;
    overflow: hidden;
    // display: inline-block;
    // opacity: .2;
    // box-shadow: 0px 0px 8px #ccc;
    
    .title {
      padding: 40px;
      color: #6a6a6a;
      font-size: 3.8em;
      font-weight: bold;
      line-height: 44px;
      // background-color: pink;
    }

    .desc {
      margin-left: 40px;
      color: #6a6a6a;
      font-size: 1.8em;
      line-height: 24px;
    }

    .go_btn {
      position: absolute;
      bottom: 40px;
      width: 170px;
      height: 46px;
      margin-left: 40px;
      border-radius: 24px;
      background: #fff;
      color: #6a6a6a;
      font-size: 2em;
      font-weight: bold;
      text-align: center;
      line-height: 50px;
    }

    // img {
    //   height: 350px;
    //   margin-left: -30px;
    // }
  }

  .mainbanner:nth-child(1) {
    background: #cadffa;
  }

  .mainbanner:nth-child(2) {
    background: #e7f8de;
  }

  .mainbanner:nth-child(3) {
    background: #fee1e6;
  }

  .mainbanner:nth-child(4) {
    background: #d9f0eb;
  }
}
</style>