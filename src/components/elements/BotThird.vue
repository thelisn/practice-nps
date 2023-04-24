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
        <div class="android">
          <img src="@/assets/images/qrcode_1.png" alt="Android">
        </div>
        <div class="ios">
          <img src="@/assets/images/qrcode_2.png" alt="iOS">
        </div>
      </div>
      <div class="txt_box">
        <p class="android_txt">Android</p>
        <p class="ios_txt">iOS</p>
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
          btn1Img: require("@/assets/images/webzine_icon1.svg"),
          btn1Text: '바로보기',
          btn2Img: require("@/assets/images/webzine_icon2.svg"),
          btn2Text: '구독하기'
        },
        {
          title: '뉴스레터',
          desc: '다양한 소식을 메일로 전하는 인터넷 소식지입니다.',
          btn1Img: require("@/assets/images/webzine_icon1.svg"),
          btn1Text: '바로보기',
          btn2Img: require("@/assets/images/webzine_icon2.svg"),
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
  margin-top: -1200px;
  transform: translateX(380px);
  // position: relative;
  // bottom: 720px;
  // background: pink;

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
      height: 40px;
      margin: 0 auto;
      // position: relative;
      // background: yellow;

      .go {
        width: 140px;
        height: 40px;
        border-radius: 20px;
        // display: inline-block;
        // height: 100%;
        // background: pink;

        img {
          padding: 6px;
          margin-left: 10px;
          // background-color: yellow;
        }

        p {
          margin-left: 20px;
          color: #fff;
          font-size: 1.4em;
          transform: translateY(-40px);
          // display: inline-block;
          // background-color: pink;
        }
      }

      .subs {
        width: 140px;
        height: 40px;
        margin-left: 10px;
        border-radius: 20px;
        // background: cornflowerblue;
        
        img {
          padding: 6px;
          margin-left: 10px;
        }

        p {
          margin-left: 20px;
          color: #fff;
          font-size: 1.4em;
          transform: translateY(-40px);
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

    .img_box {
      width: 240px;
      margin: 0 auto;
      margin-top: 15px;
      // background: pink;

      div {
        display: inline-block;
        width: 110px;
        height: 110px;
        border-radius: 20px;
        background: #eee;
      }

      .android {
        margin-right: 20px;
        
        img {
          margin: 0 auto;
          margin-top: 14px;
        }
      }

      .ios {

        img {
          margin: 0 auto;
          margin-top: 14px;
        }
      }
    }

    .txt_box {
      width: 240px;
      margin: 0 auto;
      margin-top: 8px;
      // background-color: yellow;
      
      .android_txt {
        display: inline-block;
        width: 110px;
        margin-right: 20px;
        font-size: 2em;
        text-align: center;
        // background-color: pink;
      }

      .ios_txt {
        display: inline-block;
        width: 110px;
        font-size: 2em;
        text-align: center;
        //  background-color: coral;
      }
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: calc(900px / 3 - 30px);
    transform: translateX(315px);

    .webnews_wrap {

      p {
        font-size: 1.3em;
      }

      .btn_wrap {
        width: 210px;
        // background-color: yellow;

        .go {
          width: 100px;

          img {
            margin-left: 0px;
          }

          p {
            font-size: 1.2em;
            transform: translateY(-39px);
          }
        }

        .subs {
          width: 100px;

          img {
            margin-left: 0px;
          }

          p {
            font-size: 1.2em;
          }
        }
      }
    }

    .qrcode_wrap {
      
      h2 {
        // font-size: 2.2em;
        // font-weight: bold;
      }

      .img_box {
        width: 210px;
        margin-top: 10px;
        // background-color: pink;

        div {
          width: 95px;
          height: 95px;
        }

        .android {
          
          img {
            width: 70px;
            margin-top: 15px;
          }
        }

        .ios {

          img {
            width: 70px;
            margin-top: 15px;
          }
        }
      }

      .txt_box {
        width: 210px;
        margin-top: 8px;
        // margin: 0 auto;

        .android_txt {
          width: 95px;
          font-size: 1.8em;
        }

        .ios_txt {
          width: 95px;
          font-size: 1.8em;
        }
      }
    }
  }
}

@media screen and (max-width:950px) {
  .wrap {
    width: 90%;
    transform: translateX(0px);
    margin-top: 30px;

    .webnews_wrap {
      width: calc(100% / 2 - 15px);
      display: inline-block;
      margin-right: 30px;

      p {
        font-size: 1.7em;
      }

      .btn_wrap {
        width: 250px;
        // background-color: palegoldenrod;

        .go {
          width: 120px;
        }

        .subs {
          width: 120px;
        }
      }
    }

    .webnews_wrap:nth-child(2) {
      margin-right: 0px;
    }

    .qrcode_wrap {
      .img_box {
        width: 250px;
        // background-color: pink;

        div {
          width: 115px;
          height: 115px;
        }

        .android {

          img {
            margin-top: 17px;
            width: 80px;
          }
        }

        .ios {
          img {
            width: 80px;
            margin-top: 17px;
          }
        }
      }

      .txt_box {
        width: 250px;
        margin-top: 10px;

        .android_txt {
          width: 115px;
          font-size: 2em;
        }

        .ios_txt {
          width: 115px;
          font-size: 2em;
        }
      }
    }
  }
}

@media screen and (max-width:768px) {
  .wrap {

    .webnews_wrap {
      height: 250px;

      h2 {
        font-size: 2.2em;
      }

      p {
        padding: 15px;
        // font-size: 1.4em;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }

      .btn_wrap {
        width: 120px;
        background-color: pink;

        .go {
          width: 120px;

          p {
            background: yellow;
          }
        }

        .subs {
          width: 120px;
        }
      }
    }

    .webnews_wrap:nth-child(2) {
      margin-right: 0px;
      // background-color: yellow;
    }

    .qrcode_wrap {
      .img_box {
        width: 250px;
        // background-color: pink;

        div {
          width: 115px;
          height: 115px;
        }

        .android {

          img {
            margin-top: 17px;
            width: 80px;
          }
        }

        .ios {
          img {
            width: 80px;
            margin-top: 17px;
          }
        }
      }

      .txt_box {
        width: 250px;
        margin-top: 10px;

        .android_txt {
          width: 115px;
          font-size: 2em;
        }

        .ios_txt {
          width: 115px;
          font-size: 2em;
        }
      }
    }
  }
}
</style>