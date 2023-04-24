<template>
  <div class="wrap">
    <div class="popup_wrap">
      <h2>팝업존</h2>
      <div class="popup_cont">
        <a href="#">
          <div class="box" v-for="cont in popup" :key="cont">
            <p class="title" v-html="cont.title"></p>
        <p class="desc" v-html="cont.desc"></p>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      popup: [
        {
          title: '국민연금 영상수어상단 서비스',
          desc: '국민연금에 대한 궁금증! 이제 국민연금 수어상담사와 영상으로 상담하세요!'
        },
        {
          title: '- 2022년 공공기관 종합청렴도 평가 결과 -',
          desc: '종합청렴도 2등급<br>청렴체감도 2등급 / 청렴노력도 1등급'
        },
        {
          title: '국민연금 부정수급, 지금 신고하세요!',
          desc: '부정수급자란?<br>거짓, 허위로 노령, 유족, 장애연금을 지급받고 있는 사람'
        },
        {
          title: '국민연금 적기신고 안내',
          desc: '소급분 보험료 & 과오납금 발생 예방'
        },
        {
          title: '노후긴금자금 대부가 도와드립니다.',
          desc: '대상 : 국내에 거주하는 만 60세 이상 노령, 분할, 유족, 장애(1~3급) 연금 수급자<br>금액 : 연간 연금수령액의 2배(최대 1,000만원)이내에서 실 소요 비용'
        },
        {
          title: '내 손안의 국민비서',
          desc: '국민연금(노령연금) 청구시기, 매년 인상되는 연금액을<br>국민비서로 알려드립니다!'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  position: relative;
  width: 1100px;
  height: 250px;
  margin: 0 auto;
  // top: 600px;
  // z-index: 1;
  // background: pink;

  .popup_wrap {
    width: 570px;
    height: 100%;
    margin-top: 350px;
    // position: absolute;
    // left: 0;
    // background: yellow;

    h2 {
      font-size: 2.6em;
      font-family: 'NanumSquareExtraBold';
      // font-weight: bold;
    }

    .popup_cont {

      a {

        .box  {
          position: absolute;
          bottom: 0;
          width: 570px;
          height: 200px;
          border-radius: 30px;
          // background: pink;
          // opacity: .4;

          .title {
            padding: 34px;
            color: #6a6a6a;
            font-size: 3em;
            font-family: 'NanumSquareExtraBold';
            line-height: 32px;
            // font-weight: bold;
          }

          .desc {
            margin-left: 34px;
            color: #6a6a6a;
            font-size: 1.6em;
            line-height: 26px;
          }
        }

        .box:nth-child(1) {
          background: #e0f0ff;
        }

        .box:nth-child(2) {
          background: #d9e1ff;
        }

        .box:nth-child(3) {
          background: #ffe8eb;
        }

        .box:nth-child(4) {
          background: #f0fff0;
        }

        .box:nth-child(5) {
          background: #ffffeb;
        }

        .box:nth-child(6) {
          background: #e3ffeb;
        }
      }
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: 100%;
    top: 500px;
    // transform: translateY(450px);
    // background: pink;

    .popup_wrap {
      position: relative;
      width: 90%;
      margin: 0 auto;
      
      .popup_cont {

        a {

          .box {
            width: 100%;

            .title {
              padding: 30px;
              font-size: 2.6em;
            }

            .desc {
              margin-left: 30px;
              font-size: 1.8em;
              line-height: 25px;
            }
          }
        }
      }
    }
  }
}
</style>