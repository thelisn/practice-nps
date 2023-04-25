<template>
  <div class="wrap">

    <div class="first">
      <h2>1986 ~ 1995</h2>
      <ul v-for="first in first" :key="first" class="first_list">
        <li class="first_date">{{ first.date }}</li>
        <li v-html="first.desc" class="first_desc"></li>
      </ul>
      <p class="y_1986">1986</p>
      <p class="y_1995">1995</p>
    </div>

    <div class="second">
      <h2>1996 ~ 2005</h2>
      <ul v-for="second in second" :key="second" class="second_list">
        <li class="second_date">{{ second.date }}</li>
        <li v-html="second.desc" class="second_desc"></li>
      </ul>
      <p class="y_1996">1996</p>
      <p class="y_2005">2005</p>
    </div>

    <div class="third">
      <h2>2006~</h2>
      <ul v-for="third in third" :key="third" class="third_list">
        <li class="third_date">{{ third.date }}</li>
        <li v-html="third.desc" class="third_desc"></li>
      </ul>
      <p class="y_2006">2006</p>
    </div>

  </div>
</template>

<script>

export default {
  data() {
    return {
      first: [
        {date: '1986.12.31', desc: '국민연금법 공포'},
        {date: '1987.09.18', desc: '국민연금관리공단 설립'},
        {date: '1988.01.01', desc: '국민연금제도 실시(10인 이상 사업장)'},
        {date: '1992.01.01', desc: '당연적용 사업장 확대(5인 이상 사업장)'},
        {date: '1993.01.01', desc: '특례노령연금 지급 개시'},
        {date: '1995.04.01', desc: '국민연금연구센터 설치'},
        {date: '1995.07.01', desc: '농어촌지역 주민 확대 적용'},
        {date: '1995.08.04', desc: '사업장 종사 외국인 당연 적용'}
      ],
      second: [
        {date: '1999.01.01', desc: '조기노령연금 지급 개시'},
        {date: '1999.04.01', desc: '도시지역 확대 적용(전국민 연금실시)'},
        {date: '1999.11.05', desc: '기금운용본부 설치'},
        {date: '2000.07.01', desc: '농어촌지역 특례노령연금 지급 개시'},
        {date: '2001.11.13', desc: '텔레서비스시스템 전국 확대 운영'},
        {date: '2002.11.04', desc: '4대사회보험정보연계 서비스 시행'},
        {date: '2003.01.01', desc: '감액노령연금 및 재직자노령연금 지급 개시'},
        {date: '2003.07.01', desc: '당연적용 사업장 확대 적용(1단계)<br>- 5인미만 사업장 중 법인/전문직종 사업장<br>- 5인이상 사업장의 비정규직 근로자'},
        {date: '2004.04.01', desc: '도시지역 특례노령연금 지급 개시'},
        {date: '2004.07.01', desc: '당연적용 사업장 확대 적용(2단계)<br>(국민건강보험/고용보험가입 사업장)'},
      ],
      third: [
        {date: '2006.01.01', desc: '당연적용사업장 확대적용(3단계)<br>(근로자 1인이상 사업장)'},
        {date: '2006.09.18', desc: '국민연금 新 CI발표'},
        {date: '2007.07.23', desc: '"국민연금공단"으로 명칭 변경'},
        {date: '2008.01.01', desc: '완전노령연금 지급 개시'},
        {date: '2009.05.01', desc: '노후설계서비스(CSA) 사업 시행'},
        {date: '2009.05.14', desc: '외국인 전담조직 국제업무센터 설립 및 개설'},
        {date: '2009.08.07', desc: '국민연금과 4개 직역연금 가입기간 연계사업시행'},
        {date: '2011.01.01', desc: '사회보험 징수통합에 따른 징수업무 이관'},
        {date: '2011.04.01', desc: '장애인복지법 상 장애 전(全)등급 심사 개시'},
        {date: '2011.10.05', desc: '장애인 활동지원 사업 시행'},
        {date: '2012.12.01', desc: '기초수급자 근로능력평가 사업 수행'},
        {date: '2014.07.01', desc: '기초연금 사업 수행'},
        {date: '2015.12.23', desc: '전 국민 대상 노후준비서비스 시행'}
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  width: 80%;
  height: 2015px;
  margin: 0 auto;
  // background-color: yellow;

  h2 {
    height: 500px;
    font-size: 4.2em;
    font-family: 'NanumSquareExtraBold';
    // font-weight: bold;
    // background-color: yellow;
    display: inline-block;

    &::after {
      display: block;
      position: absolute;
      top: 10px;
      left: 250px;
      border-radius: 5px;
      width: 10px;
      height: 10px;
      content: '';
      background: #92a8d1;
    }
  }

    .y_1986,
    .y_1995,
    .y_1996,
    .y_2005,
    .y_2006
     {
      position: absolute;
      right: 0;
      // display: inline-block;
      font-family: 'NanumSquareExtraBold';
      font-size: 10em;
      opacity: .1;
      // background-color: yellow;
    }

    .y_1986,
    .y_1996,
    .y_2006 {
      top: 0;
    }

  .first {
    width: 100%;
    position: relative;
    height: 500px;
    // background: pink;
    margin-bottom: 30px;

    .first_list {
      width: 800px;
      // background: coral;
      position: relative;
      top: -495px;
      left: 300px;
      // position: absolute;
      // height: 500px;

      &::before {
        content: '';
        display: block;
        top: 10px;
        right: 845px;
        z-index: -9;
        position: absolute;
        width: 1px;
        height: 1600px;
        // height: 300px;
        // background: #ccc;
        background: linear-gradient(#f7cac9, #92a8d1);
      }

      .first_date {
        width: 100px;
        // background-color: salmon;
        font-size: 2.2em;
        display: inline-block;
        margin-bottom: 30px;
        margin-right: 40px;

      }

      .first_desc {
        font-size: 2em;
        line-height: 30px;
        display: inline-block;
        // background: palevioletred;
      }
    }

    .y_1995 {
      top: 340px;
    }
  }

  .second {
    width: 100%;
    position: relative;
    height: 700px;
    margin-bottom: 30px;
    // background-color: pink;

    .second_list {
      width: 800px;
      position: relative;
      top: -495px;
      left: 300px;

      &:nth-child(9) {
        .second_date {
          transform: translateY(-60px);
        }
      }

      &:nth-child(11) {
        .second_date {
          transform: translateY(-30px);
        }
      }

      .second_date {
        width: 100px;
        font-size: 2.2em;
        display: inline-block;
        margin-bottom: 30px;
        margin-right: 40px;
        // background-color: salmon;
      }

      .second_desc {
        font-size: 2em;
        line-height: 30px;
        display: inline-block;
        // background-color: palegoldenrod;
      }
    }

    .y_2005 {
      top: 540px;
    }
  }

  .third {
    width: 100%;
    height: 500px;
    position: relative;
    
    .third_list {
      // background-color: pink;
      width: 800px;
      position: relative;
      top: -495px;
      left: 300px;

      &:nth-child(2) {
        .third_date {
          transform: translateY(-30px);
        }
      }

      .third_date {
        width: 100px;
        font-size: 2.2em;
        display: inline-block;
        margin-bottom: 30px;
        margin-right: 40px;
      }

      .third_desc {
        line-height: 30px;
        font-size: 2em;
        display: inline-block;
      }
    }
  }
}

@media screen and (max-width:950px) {
  .wrap {
    width: 90%;

    h2 {
      // height: 00px;
      display: block;
      margin-left: 20px;
      // background-color: yellow;

      &::after {
        top: 70px;
        left: 0;
      }
    }

    .first {
      // background-color: pink;
      margin-bottom: 20px;

      .first_list {
        // background-color: pink;
        top: -400px;
        left: 0;

        &::before {
          left: 4px;
          top: -30px;
          height: 1550px;
        }

        .first_date {
          margin-left: 20px;
          font-size: 2em;
          // width: 90px;
          // background-color: pink;
          margin-bottom: 20px;
        }

        .first_desc {
          font-size: 1.6em;
        }
      }

      .y_1995 {
        top: 350px;
      }
    }

    .second {
      margin-bottom: 20px;

      .second_list {
        top: -400px;
        left: 0;

        .second_date {
          margin-left: 20px;
          font-size: 2em;
          margin-bottom: 20px;
        }

        .second_desc {
          font-size: 1.6em;
        }
      }

      .y_2005 {
        top: 530px;
      }
    }

    .third {

      .third_list {
        left: 0;
        top: -400px;

        .third_date {
          font-size: 2em;
          margin-bottom: 20px;
          margin-left: 20px;
        }

        .third_desc {
          font-size: 1.6em;
        }
      }
    }
  }
}
</style>