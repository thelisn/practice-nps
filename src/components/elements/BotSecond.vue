<template>
  <div class="wrap">
    <div class="video_wrap border_box">
      <h2 class="title1">영상으로 보는 국민연금</h2>
      <a href="#">
        <div class="video_img"></div>
      </a>
      <p class="desc">국민연금공단과 필쩐필승이 만났다!</p>
    </div>

    <div class="cardnews_wrap border_box">
      <h2 class="title2">카드뉴스</h2>
      <a href="#">
        <div class="news_img"></div>
      </a>
    </div>
    
  </div>
</template>

<script>
</script>

<style scoped lang="scss">
.wrap {
  width: calc(1100px / 3 - 30px);
  margin: 0 auto;
  transform: translateY(-600px);
  // width: calc(80% / 3 - 30px);
  // background: pink;

  .border_box {
    border: 1px solid #ccc;
    border-radius: 20px;
  }

  .video_wrap {
    width: 100%;
    height: 350px;
    background: #fff;

    .title1 {
      margin-top: 30px;
      margin-bottom: 20px;
      font-size: 2.6em;
      text-align: center;
      // padding: 40px;
      // background: yellow;
    }

    a {

      .video_img {
        overflow: hidden;
        width: 90%;
        height: 170px;
        margin: 0 auto;
        border-radius: 20px;
        background: url(@/assets/images/video.png) no-repeat center/cover;
        // background: green;
      }
    }

    .desc {
      margin-top: 30px;
      font-size: 1.8em;
      font-family: 'NanumBarunGothicLight';
      text-align: center;
      //!!!!!! 폰트 수정
      // padding: 40px;
      // background: yellow;
    }
  }

  .cardnews_wrap {
    width: 100%;
    height: 220px;
    margin-top: 30px;
    background: #fff;

    .title2 {
      margin-top: 30px;
      margin-bottom: 20px;
      font-size: 2.6em;
      text-align: center;
    }

    a {

      .news_img {
        overflow: hidden;
        width: 90%;
        height: 110px;
        margin: 0 auto;
        border-radius: 20px;
        background: url(@/assets/images/cardnews.png) no-repeat center/cover;
        // background: green;
      }
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: calc(900px / 3 - 30px);
  }
}

@media screen and (max-width:950px) {
  .wrap {
    width: 90%;
    margin-top: 30px;
    transform: translateY(0px);
    // display: none;

    .video_wrap {
      height: 650px;
      // width: 100%;

      a {

        .video_img {
          height: 500px;
        }
      }

      .desc {
        font-size: 2.2em;
      }
    }

    .cardnews_wrap {
      height: 400px;

      a {

        .news_img {
          height: 300px;
        }
      }
    }
  }
}

</style>