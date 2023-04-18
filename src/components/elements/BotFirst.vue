<template>
  <div class="wrap">
    <div class="top_wrap">
      <div class="top_cont border_box" v-for="item in top" :key="item">
        <a href="#">
          <div class="text">
            <p class="title1">{{ item }}</p>
            <button class="btn">&#10095;</button>
          </div>
        </a>
      </div>
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
  // position: relative;
  // top: 480px;
  // width: calc(80% / 3 - 30px);
  width: calc(1100px / 3 - 30px);
  margin: 0 auto;
  margin-top: 50px;
  transform: translateX(-380px);
  // background: pink;
  // height: 500px;

  .border_box {
    border: 1px solid #ccc;
    border-radius: 20px;
  }

  .top_wrap {
    width: 100%;
    // background: beige;

    .top_cont {
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
        font-size: 2.4em;
        // color: #000;
        // background-color: yellow;
      }

      .more {
        width: 90px;
        height: 40px;
        margin-left:10px;
        border: 1px solid #ccc;
        border-radius: 20px;
        background: #fff;
        color: #6a6a6a;
        font-size: 1.8em;
        line-height: 30px;
        transition: .3s;
        // padding: 20px;
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
</style>