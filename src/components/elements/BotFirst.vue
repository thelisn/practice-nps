<template>
  <div class="wrap">
    <div class="top_wrap">
      <dv class="top_cont border_box" v-for="item in top" :key="item">
        <a href="#">
          <div class="text">
            <p class="title1">{{ item }}</p>
            <button class="btn">&#10095;</button>
          </div>
        </a>
      </dv>
    </div>
    
    <div class="onair_wrap">
      <div class="onair_cont border_box">
        <p class="title2">국민연금 ON AIR</p>
        <button class="more">+ 더보기</button>
        <ul class="onair_list">
          <li>
            <a href="#">- 국민연금제도</a>
          </li>
          <li>
            <a href="#">- 국민연금 Basic</a>
          </li>
          <li>
            <a href="#">- 전문가 시선</a>
          </li>
          <li>
            <a href="#">- 국민연금 기금</a>
          </li>
          <li>
            <a href="#">- 영상갤러리</a>
          </li>
        </ul>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      top: ['사회보장 협정', '세계의 연금제도', '권리구제 제도 안내']
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  width: calc(1100px / 3 - 30px);
  margin: 0 auto;
  margin-top: 60px;
  transform: translateX(-380px);
  // position: relative;
  // top: 480px;
  // width: calc(80% / 3 - 30px);
  // height: 500px;
  // background: pink;

  .border_box {
    border: 1px solid #ccc;
    border-radius: 20px;
  }

  .top_wrap {
    width: 100%;
    // background: beige;

    .top_cont {
      display: block;
      width: 100%;
      height: 60px;
      margin-bottom: 20px;
      background: #fff;
      transition: .3s;
      // border-radius: 20px;
      // background: yellow;

      &:hover {
        background: #eee;
      }

      a {

        .text {
            
          .title1 {
            display: inline-block;
            padding: 21px;
            color: #6a6a6a;
            font-size: 2em;
            font-weight: 700;
          }
            
          .btn {
            position: absolute;
            right: 0px;
            padding: 17px;
            color: #6a6a6a;
            font-size: 2.4em;
          }
        }
      }
    }
  }

  .onair_wrap {

    .onair_cont {
      width: 100%;
      height: 350px;
      margin-top: 30px;
      background: #fff7f7;

      .title2 {
        display: inline-block;
        padding: 25px;
        font-size: 2.6em;
        // background-color: yellow;
        // color: #000;
      }

      .more {
        width: 90px;
        height: 40px;
        border: 1px solid #ccc;
        border-radius: 20px;
        background: #fff;
        color: #6a6a6a;
        font-size: 1.8em;
        line-height: 30px;
        transition: .3s;
        // padding: 20px;
        // margin-left:20px;
        // text-align: center;

        &:hover {
          border: 1px solid #666;
          background: #666;
          color: #fff;
        }
      }

      .onair_list {
        margin-top: 20px;
        font-weight: 100;
        // background: pink;

        li {

          a {
            margin-left: 20px;
            color: #6a6a6a;
            font-size: 2em;
            line-height: 40px;
          }
        }
      }
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: calc(900px / 3 - 30px);
    transform: translateX(-315px);

    .more {
      margin-left: 20px;
    }
  }
}

@media screen and (max-width:950px) {
  .wrap {
    margin-top: 30px;
    width: 90%;
    transform: translateX(0px);
    // background: pink;

    .top_wrap {
      // background-color: beige;

      .top_cont {
        width: calc(100% / 2 - 15px);
        display: inline-block;
        margin-right: 30px;
        margin-bottom: 0px;
        
        a {
          position: relative;
        }
      }

      .top_cont:nth-child(2) {
        margin-right: 0px;
      }
      .top_cont:nth-child(3) {
        display: none;
      }
    }

    .onair_wrap {
      display: none;
    }
  }
}
</style>