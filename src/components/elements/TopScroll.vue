<template>
  <div class="top_scroll">
    <div class="top_box">
      <div class="title">공단사이트</div>
      <div class="list">
      <p v-for="btnList in btnList" :key="btnList">
      <a href="#" v-html="btnList"></a></p>
      </div>
      <button class="more">+ 더보기</button>
    </div>
    <button class="top">
      <p>&uarr;</p>
      <p>TOP</p>
    </button>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      btnList: ['전자민원서비스', '중앙노후준비<br>지원센터', '국민연금 EDI', '기금운용본부', '연금수급자', '국민연금연구원', 'ESG경영', '장애인활동지원', '스마트 위택스', '어린이', '4대보험정보연계', '기초연금', '두루누리사회보험', '공적연금 연계', '청풍리조트']
    }
  }
}

</script>

<style scoped lang="scss">
.top_scroll {
  position: fixed;
  top: 25%;
  right: 20px;
  z-index: 9999;
  .top_box {
    background: white;
    width: 130px;
    height: 350px;
    border-radius: 20px;
    box-shadow: 2px 2px 10px #ccc;

    .title {
      // display: none;
      transform: translateY(15px);
      margin: 0 auto;
      width: 100px;
      height: 40px;
      border-radius: 15px;
      background: #d5e3fb;
      font-size: 1.6em;
      color: #3e65c9;
      font-weight: bold;
      padding: 15px;
    }

    p:nth-child(1) {
      margin-top: 40px;
    }

    p {
      line-height: 20px;
      // margin-top: 40px;
      margin-bottom: 20px;
      text-align: center;
      
      a {
      font-size: 1.6em;
      color: #6a6a6a;

      &:hover {
        color: #000;
      }
    }
  }

  p:nth-child(6),
  p:nth-child(7),
  p:nth-child(8),
  p:nth-child(9),
  p:nth-child(10),
  p:nth-child(11),
  p:nth-child(12),
  p:nth-child(13),
  p:nth-child(14),
  p:nth-child(15) {
    display: none;
  }

  .more {
    background: gray;
    width: 100px;
    height: 30px;
    border-radius: 15px;
    color: #fff;
    font-size: 1.6em;
    text-align: center;
    margin-left: 50%;
    transform: translateX(-50%);
    transition: .3s;
    margin-top: -3px;

    &:hover {
      background: #555
    }
  }

  }

  .top {
    width: 50px;
    height: 50px;
    margin-top: 10px;
    position: relative;
    transform: translateX(-50%);
    left: 50%;
    border-radius: 25px;
    background: #333;

    p {
      color: #fff;
      font-size: .9em;
      font-weight: bold;
    }
  }
}

@media screen and (max-width:1440px) {
  .top_scroll {
    display: none;
  }
}
</style>