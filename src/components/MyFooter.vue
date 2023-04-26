<template>
  <div class="footer">
    <hr>
    <div class="center">
      <div class="center_box">
        <img src="@/assets/images/f_center_icon.svg" alt="국민연금 고객센터">
      </div>
      <p><span>국민연금 고객센터 &#8594;</span> 국번없이 <span>1</span><span>3</span><span>55</span>(유료) 해외 +82-63-713-6900 / <span>평일 09:00 ~ 18:00</span></p>
    </div>
    <a href="#" class="video" onclick="return false">
      <div class="video_box">
        <img src="@/assets/images/f_video_icon.svg" alt="영상수어상담">
      </div>
      <p>영상수어상담 &#8594;</p>
    </a>
    <div class="bar">
      <div class="txt">
        <a href="#" v-for="txt in txt" :key="txt">
          <p>{{ txt }}</p>
        </a>
      </div>

      <div class="sns">
        <div class="sns_box" v-for="img in img" :key="img">
          <a href="#">
            <img :src="img" alt="sns아이콘">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      txt: ['개인정보처리방침', '이용약관', '홈페이지 이용안내', '홈페이지 개선의견', 'RSS', '찾아오시는 길', '인증서 모바일로 내보내기'],
      img: [
        require("@/assets/images/f_sns1.svg"),
        require("@/assets/images/f_sns2.svg"),
        require("@/assets/images/f_sns3.svg"),
        require("@/assets/images/f_sns4.svg"),
        require("@/assets/images/f_sns5.svg"),
        require("@/assets/images/f_sns6.svg")
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.footer {
  position: relative;
  width: 1100px;
  margin: 0 auto;
  margin-top: 80px;
  margin-bottom: 30px;
  // background: #ccc;

  hr {
    height:1px;
    margin-bottom: 60px;
    border: 0;
    background: #ddd;
  }

  .center {

    .center_box {
      display: inline-block;
      width: 30px;
      height: 30px;
      border-radius: 10px;
      background-color: #008000;

      img {
        width: 15px;
        margin: 0 auto;
        transform: translateY(7px);
        // background-color: pink;
      }
    }

    p {
      display: inline-block;
      margin-left: 10px;
      font-size: 2.2em;
      font-family: 'NanumSquareBold';
      transform: translateY(-8px);
      // background-color: pink;

      span:nth-child(1) {
        color: #008000;
      }

      span:nth-child(2) {
        color: #d13800;
      }

      span:nth-child(3) {
        color: #008000;
      }

      span:nth-child(4) {
        color: #0000bb;
      }
    }
  }

  .video {
    position: absolute;
    top: 60px;
    right: 0;

    .video_box {
      display: inline-block;
      width: 30px;
      height: 30px;
      border-radius: 10px;
      background: #0000bb;

      img {
        width: 15px;
        margin: 0 auto;
        transform: translateY(7px);
      }
    }

    p {
      display: inline-block;
      margin-left: 10px;
      color: #0000bb;
      font-size: 2.2em;
      font-family: 'NanumSquareBold';
      transform: translateY(-8px);
      // background-color: pink;
    }
  }

  .bar {
    position: relative;
    width: 100%;
    height: 70px;
    margin-top: 30px;
    border-radius: 15px;
    background: #eee;

    a {
      display: inline-block;
    }

    .txt {
      width:750px;
      height: 100%;
      margin-left: 20px;
      // background: yellow;
      
      a {
        margin-right: 26px;
        
        &:nth-child(1) {
          
          p {
            color: #0000bb;
            font-family: 'NanumSquareBold';
          }
        }

        p {
          font-size: 1.4em;
          line-height: 70px;
          // background: pink;
        }
      }

      a:nth-child(7) {
        margin-right: 0px;
      }
    }

    .sns {
      position: absolute;
      top: 0;
      right: 20px;
      width: 300px;
      height: 100%;
      // background-color: pink;

        .sns_box {
          display: inline-block;
          width: 40px;
          height: 40px;
          margin-top: 12px;
          margin-right: 10px;
          border: 1px solid #ccc;
          border-radius: 20px;
          background: #fff;

          &:last-child {
            margin-right: 0px;   
          }

          &:hover img {
            transform: scale(1.1);
          }
          
          a {
          width: 100%;
          // line-height: 75px;
          // margin-right: 10px;
          // background-color: pink;
          
          img {
            width:100%;
            transition: .2s;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 1200px) {
  .footer {
    width: 90%;

    .center {

      .center_box {
        width: 26px;
        height: 26px;
        border-radius: 8px;

        img {
          width: 13px;
        }
      }

      p {
        margin-left: 8px;
        font-size: 1.8em;
      }
    }

    .video {

      .video_box {
        width: 26px;
        height: 26px;
        border-radius: 8px;

        img {
          width: 13px;
        }
      }

      p {
        margin-left: 8px;
        font-size: 1.8em;
      }
    }

    .bar {

      .txt {

        a {

          &:nth-child(3),
          &:nth-child(6),
          &:nth-child(7) {
            display: none;
          }

          p {
            font-size: 1.3em;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 950px) {
  .footer {

    hr {
      margin-bottom: 40px;
    }

    .center {

      p {
        margin-left: 20px;
        font-size: 1.6em;
        line-height: 20px;
        transform: translateY(28px);
        // background-color: pink;

        span:nth-child(1) {
          display: block;
        }

        span:nth-child(5) {
          display: block;
        }
      }
    }

    .video {
      top: 160px;
      left: 0;

      p {
        margin-left: 20px;
        font-size: 1.6em;
      }
    }

    .bar {
      height: 120px;
      margin-top: 120px;

      .txt {
        width: 100%;
        margin-left: 0px;
        text-align: center;
        // background-color: pink;

        a {

          p {
            font-size: 1.6em;
          }
        }
      }

      .sns {
        top: 50px;
        left: 50%;
        transform: translateX(-50%);
      }
    }
  }
}
</style>