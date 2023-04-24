<template>
  <div class="wrap">
    <div class="cont" v-for="cont in puzzle" :key="cont">
      <p class="title">{{ cont.title }}</p>
      <ul class="desc">
        <li>{{ cont.desc[0] }}</li>
        <li>{{ cont.desc[1] }}</li>
        <li>{{ cont.desc[2] }}</li>
        <li>{{ cont.desc[3] }}</li>
        <li>{{ cont.desc[4] }}</li>
        <li>{{ cont.desc[5] }}</li>
      </ul>
    </div>
    <div class="circle_green"></div>
    <div class="circle_red"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      puzzle: [
        {
          title: '장애인 & 복지서비스',
          desc: ['- 장애인 지원사업 안내', '- 장애인 활동지원', '- 기초수급자 근로능력평가', '- 기초연금']
        },
        {
          title: '국민연금 100문 100답',
          desc: ['- 연금제도', '- 가입 관련', '- 보험료 부과', '- 연금 지급']
        },
        {
          title: '제 5차 재정 계산', 
          desc: ['- 추진 개요', '- 추진 체계', '- 재정 계산 위원회', '- 국민연금 전문가포럼', '- 보도자료', '- 영상자료']
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  width: 1100px;
  height: 300px;
  margin: 0 auto;
  margin-top: 60px;
  // position: relative;
  // top: 440px;
  // background: pink;
  // margin-bottom: 100px;

  .cont {
    float: left;
    width: calc(100% / 3 - 30px);
    height: 100%;
    margin-right: 45px;
    border-radius: 30px;
    // display: inline-block;
    // margin-top: 30px;
    // background: green;

    .title {
      padding: 30px;
      color: #fff;
      font-size: 2.6em;
      font-family: 'NanumSquareExtraBold';
      // font-weight: bold;
    }

    .desc {

      li {
        margin-bottom: 18px;
        margin-left: 60px;
        color: #fff;
        font-size: 1.8em;
        // font-family: 'NanumSquareBold';
        // font-weight: 400;
        // background: yellow;
        // line-height: 35px;
        // cursor: pointer;
      }
    }
  }

  .cont:nth-child(1) {
    position: relative;
    z-index: 1;
    background: linear-gradient(145deg, #07ae41 40%, #85e7a2);
  }

  .cont:nth-child(2) {
    background: linear-gradient(145deg, #358ce3 50%, #a3cefe);
  }

  .cont:nth-child(3) {
    position: relative;
    z-index: 1;
    background: linear-gradient(145deg, #d65b3c 50%, #f6a886);
  }

  .cont:nth-child(3) {
    margin-right: 0px;
  }

  .circle_green {
    position: relative;
    top: 130px;
    left: 265px;
    width: 150px;
    height: 150px;
    border: 20px solid #fff;
    border-radius: 100px;
    background: linear-gradient(145deg, #65d587 40%, #7fe59d)
  }

  .circle_red {
    position: relative;
    top:-120px;
    left: 685px;
    width: 150px;
    height: 150px;
    border: 20px solid #fff;
    border-radius: 100px;
    background: #d65b3c;
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: 900px;
    top: 600px;

    .cont {

      .title {
        font-size: 2.4em;
      }
    }

    .circle_green {
      left: 205px;
      width: 140px;
      height: 140px;
      border: 20px solid #fff;
      border-radius: 70px;
    }

    .circle_red {
      left: 555px;
      width: 140px;
      height: 140px;
      border: 20px solid #fff;
      border-radius: 70px;
    }
  }
}

@media screen and (max-width:950px) {
  .wrap {
    width: 100%;
    height: 405px;
    margin-top: 50px;
    // background: pink;

    .cont {
      position: relative;
      left: 50%;
      width: 90%;
      height: 180px;
      margin-right: 0px;
      margin-bottom: 15px;
      transform: translateX(-50%);

      .title {
        font-size: 2.2em;
      }

      .desc {
        display: flex;
        flex-wrap: wrap;

        li {
          width: 40%;
          margin: 0 auto;
          margin-bottom: 25px;
          // background: pink;
        }
      }
    }

    .cont:nth-child(1),
    .circle_green,
    .circle_red {
      display: none;
    }

    .cont:nth-child(3) {
      height: 210px;
    }
  }
}
</style>