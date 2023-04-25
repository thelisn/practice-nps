<template>
  <div class="footer">
    <hr>
    <div class="center">
      <div class="center_box">
      <img src="@/assets/images/f_center_icon.svg" alt="국민연금 고객센터">
      </div>
      <p><span>국민연금 고객센터 &#8594;</span> 국번없이 <span>1</span><span>3</span><span>55</span>(유료) 해외 +82-63-713-6900 / 평일 09:00 ~ 18:00</p>
    </div>
    <a href="#" class="video" onclick="return false">
      <div class="video_box"><img src="@/assets/images/f_video_icon.svg" alt="영상수어상담"></div>
      <p>영상수어상담 &#8594;</p>
    </a>
    <div class="bar">
      <div class="txt">
      <a href="#" v-for="txt in txt" :key="txt"><p>{{ txt }}</p></a>
      </div>

      <div class="sns">
      <a href="#"><div class="sns_box" v-for="img in img" :key="img">
        <img :src="img" alt="sns아이콘">
      </div></a>
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
  background: #ccc;
  margin-top: 60px;
  margin-bottom: 100px;

  hr {
    margin-bottom: 60px;
  }

  .center {

    .center_box {
      width: 30px;
      height: 30px;
      border-radius: 10px;
      background-color: green;
    }

    p {
      font-family: 'NanumSquareBold';
      font-size: 2.2em;

      span:nth-child(1) {
        color: green;
      }

      span:nth-child(2) {
        color: orangered;
      }

      span:nth-child(3) {
        color: green;
      }

      span:nth-child(4) {
        color: blue;
      }
    }
  }

  .video {
    position: absolute;
    top: 60px;
    right: 0;

    p {
      font-size: 2.2em;
      color: blue;
      font-family: 'NanumSquareBold';
    }
  }

  .bar {
    position: relative;
    width: 100%;
    height: 70px;
    margin-top: 30px;
    background: #eee;
    border-radius: 15px;

    a {
      display: inline-block;
    }

    .txt {
      background: yellow;
      width:750px;
      height: 100%;
      margin-left: 30px;

      a {
        margin-right: 26px;

        &:nth-child(1) {
          p {
            color: blue;
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
      background-color: pink;

      a {
        line-height: 75px;
        margin-right: 10px;
      }
    }
  }
}
</style>