<template>
  <div class="wrap">
    <div v-for="cont in webnews" :key="cont" class="webnews_wrap border_box">
      <h2>{{ cont.title }}</h2>
      <p>{{ cont.desc }}</p>
      <div class="btn_wrap">
        <button class="go">
          <img :src="cont.btn1Img" alt="바로보기">
          <p>{{ cont.btn1Text }}</p>
        </button>
        <button class="subs">
          <img :src="cont.btn2Img" alt="구독하기">
          <p>{{ cont.btn2Text }}</p>
        </button>
      </div>
    </div>

    <div class="qrcode_wrap border_box">
      <h2>내 곁에 국민연금 APP 다운로드</h2>
      <div class="img_box">
        <img src="" alt="Android">
        <img src="" alt="iOS">
      </div>
    </div>


    
  </div>
</template>

<script>
export default {
  data() {
    return {
      webnews: [
        {
          title: "웹진 '내 곁에 국민연금'",
          desc: '새롭게 단장한 웹진을 만나보세요.',
          btn1Img: '@',
          btn1Text: '바로보기',
          btn2Img: '@',
          btn2Text: '구독하기'
        },
        {
          title: '뉴스레터',
          desc: '다양한 소식을 메일로 전하는 인터넷 소식지입니다.',
          btn1Img: '@',
          btn1Text: '바로보기',
          btn2Img: '@',
          btn2Text: '구독하기'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  width: calc(1100px / 3 - 30px);
  margin: 0 auto;
  // background: pink;

  // position: relative;
  // bottom: 720px;

  transform: translateX(380px);
  
  margin-top: -1200px;

  .border_box {
    border: 1px solid #ccc;
    border-radius: 20px;
  }

  .webnews_wrap {
    width: 100%;
    height: 160px;
    margin-bottom: 30px;
    background: #fff6f8;
    // background: #fff;

    h2 {
      margin-top: 30px;
      font-size: 2.6em;
      text-align: center;
    }

    p {
      margin-top: 10px;
      margin-bottom: 10px;
      font-size: 1.6em;
      font-family: 'NanumBarunGothic';
      text-align: center;
    }
    
    .btn_wrap {
      width: 290px;
      margin: 0 auto;
      // background: yellow;

      .go {
        width: 140px;
        height: 40px;
        border-radius: 25px;
        // background: pink;

        p {
          color: #fff;
          font-size: 1.4em;
        }
      }

      .subs {
        width: 140px;
        height: 40px;
        margin-left: 10px;
        border-radius: 25px;
        // background: cornflowerblue;

        p {
          color: #fff;
          font-size: 1.4em;
        }
      }
    }
  }

  .webnews_wrap:nth-child(1) {
    .go,
    .subs {
      background: #ee7296;
    }
  }

  .webnews_wrap:nth-child(2) {
    .go,
    .subs {
      background: #6280b8;
    }
  }

  .qrcode_wrap {
    width: 100%;
    height: 220px;
    background: #fff;

    h2 {
      margin-top: 30px;
      font-size: 2.6em;
      text-align: center;
    }
  }
}
</style>