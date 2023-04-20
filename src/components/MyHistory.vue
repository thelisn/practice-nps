<template>
  <div class="wrap">

    <div class="first">
      <h2>1986 ~ 1995</h2>
      <ul v-for="first in first" :key="first" class="first_list">
        <li class="first_date">{{ first.date }}</li>
        <li v-html="first.desc" class="first_desc"></li>
      </ul>
      <p class="1986">1986</p>
      <p class="1995">1995</p>
    </div>

    <div class="second">
      <h2>1996 ~ 2005</h2>
      <ul v-for="second in second" :key="second" class="second_list">
        <li class="second_date">{{ second.date }}</li>
        <li v-html="second.desc" class="second_desc"></li>
      </ul>
    </div>

    <div class="third">
      <h2>2006~</h2>
      <ul v-for="third in third" :key="third" class="third_list">
        <li class="third_date">{{ third.date }}</li>
        <li v-html="third.desc" class="third_desc"></li>
      </ul>
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
        {date: '2006.09.18', desc: '국민연금 한자(신) CI발표'},
        {date: '2007.07.23', desc: '"국민연금공단"으로 명칭 변경'},
        {date: '2008.01.01', desc: '완전노령연금 지급 개시'},
        {date: '2009.05.01', desc: '노후설계서비스(CSA) 사업 시행'},
        {date: '2009.05.14', desc: '외국인 전담조직 국제업무센터 설립 및 개설'},
        {date: '2009.08.07', desc: '국민연금과 4개 직역연금 가입기간 연계사업시행'},
        {date: '2011.01.01', desc: '사회보험 징수통합에 따른 징수업무 이관'},
        {date: '2011.04.01', desc: '장애인복지법 상 장애 전(한자)등급 심사 개시'},
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
  margin: 0 auto;

  h2 {
    height: 500px;
    font-size: 4.2em;
    font-weight: bold;
    // background-color: yellow;
    display: inline-block;
  }

  .first {
    width: 100%;
    position: relative;
    height: 500px;
    // background: pink;
    margin-bottom: 30px;

    .first_list {
      width: 500px;
      // background: coral;
      position: relative;
      top: -490px;
      left: 300px;
      // position: absolute;
      // height: 500px;

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
        display: inline-block;
        // background: palevioletred;
      }
    }
  }

  .second {
    width: 100%;
    position: relative;
    height: 700px;
    margin-bottom: 30px;
    // background-color: pink;

    .second_list {
      width: 500px;
      position: relative;
      top: -490px;
      left: 300px;

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
        display: inline-block;
        // background-color: palegoldenrod;
      }
    }
  }

  .third {
    width: 100%;
    height: 500px;
    position: relative;
    
    .third_list {
      width: 500px;
      position: relative;
      top: -490px;
      left: 300px;

      .third_date {
        width: 100px;
        font-size: 2.2em;
        display: inline-block;
        margin-bottom: 30px;
        margin-right: 40px;
      }

      .third_desc {
        font-size: 2em;
        display: inline-block;
      }
    }
  }
}
</style>