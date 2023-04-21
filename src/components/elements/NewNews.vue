<template>
  <div class="wrap">
    <div class="listbtn_wrap">
      <ul class="listbtn">
        <a href="#" onclick="return false">
          <li v-for="list in list" :key="list">{{ list.listCategory }}</li>
        </a>
      </ul>
    </div>

    <div class="cont_wrap">
      <a href="#">
      <div 
        class="cont" 
        :v-for="(contIndex, cont) in list" 
        :key="`contIndex-${contIndex}`"
      >
        <div 
          class="data-repeat" 
          :v-for="(contDataIndex, contData) in cont.data" 
          :key="`contDataIndex-${contDataIndex}`"
        >
          <h3 class="title">{{ contData.title }}</h3>
          <p 
            v-if="contData.newCheck === true"
            class="newCheck" 
          >
            NEW
          </p>
          <p class="date">{{ contData.date }}</p>
        </div>
      </div>
      </a>
    </div>

  </div> <!-- wrap -->
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          listCategory: '새소식',
          data: [
            {
              title: '국민연금공단 세종사옥 신규 임대 안내',
              date: '2023-04-20',
              newCheck: true,
            },
            {
              title: '국민연금공단 사칭 문자(스미싱) 주의 안내',
              date: '2023-04-12',
              newCheck: false,
            },
            {
              title: '2023년도 국민연금 기준소득월액 상/하한액 조정 안내',
              date: '2023-04-05',
              newCheck: false,
            },
            {
              title: '2022년 우수 국민제안 심사위원회 결과 안내',
              date: '2023-03-24',
              newCheck: false,
            },
            {
              title: '2022년 제1차 국민연금 토론방 토론우수자 선정 및 기념품 당...',
              date: '2023-02-27',
              newCheck: false,
            }
          ],
        }, // 새소식

        {
          listCategory: '보도자료',
          data: [{
            title: '[보도자료] 국민연금, 동반성장 평가 2년 연속 "최우수" 등급...',
            date: '2023-04-21',
            newCheck: true,
          },
          {
            title: '[보도자료] 국민연금공단, "공공데이터 제공 운영실태 평가" 4...',
            date: '2023-04-20',
            newCheck: true,
          },
          {
            title: '[보도자료] BNY멜론 자산운용그룹, 전주사무소 개소...국민연금...',
            date: '2023-04-19',
            newCheck: true,
          },
          {
            title: '[보도자료] 국민연금/한국은행 350억달러 외환 스왑 한도 합의',
            date: '2023-04-13'
          }
          ]
        }, // 보도자료

        {
          listCategory: '채용공고',
          data: [{
            title: '국민연금공단 공무직(사서직) 및 기간제 근로자(기록연구직, 고객...',
            date: '2023-04-12',
            newCheck: false,
          },
          {
            title: '[국민연금공단 대구지역본부] 공무직(환경관리직) 공개 채용',
            date: '2023-04-10',
            newCheck: false,
          },
          {
            title: '[국민연금공단 경인지역본부] 공무직(시설직) 공개채용',
            date: '2023-04-10',
            newCheck: false,
          },
          {
            title: '[국민연금공단 대전세종지역본부] 공무직(환경관리직, 시설직) 공개...',
            date: '2023-04-06',
            newCheck: false,
          },
          {
            title: '[국민연금공단 부산지역본부] 공무직(시설직) 공개채용 공고',
            date: '2023-04-06',
            newCheck: false,
          }
          ]
        }, // 채용공고

        {
          listCategory: '입찰공고',
          data: [
            {
              title: '2023년도 청풍리조트 전기안전관리자 위탁성주 용역 계약(재공고...',
              date: '2023-04-20',
              newCheck: true,
            },
            {
              title: '2023년 청풍리조트 사업장 생활계폐기물 처리 용역 단가 계약',
              date: '2023-04-17',
              newCheck: false,
            },
            {
              title: '공익형 사옥 건립 타당성 조사 연구용역',
              date: '2023-04-13',
              newCheck: false,
            },
            {
              title: '통계 소프트웨어 갱신(SAS)',
              date: '2023-04-12',
              newCheck: false,
            },
            {
              title: '국민연금공단 서울남부지역본부 불용차량 매각 재공고',
              date: '2023-04-11',
              newCheck: false,
            }
          ]
        }, // 입찰공고
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  position: relative;
  top: 300px;
  // background: pink;
  width: 1100px;
  height: 220px;
  margin: 0 auto;

  .listbtn_wrap {
    width: 400px;
    height: 50px;
    border-radius: 25px;
    background: #eee;

    .listbtn {

      // width: 100px;
      // height: 100px;
      // background-color: ivory;
      // display: inline-block;
      a {
        li {
          display: inline-block;
          width: 100px;
          height: 50px;
          border-radius: 25px;
          font-size: 1.6em; // font-family: 'NanumBarunGothic';
          text-align: center;
          line-height: 55px;
          cursor: pointer;
          transition: .2s; // margin-right: 20px;

          // background-color: yellow;
          &:hover {
            color: #fff;
          }
        }

        li:nth-child(1) {
          &:hover {
            background: #ef681e;
          }
        }

        li:nth-child(2) {
          &:hover {
            background: #6992dd;
          }
        }

        li:nth-child(3) {
          &:hover {
            background: #20aa20;
          }
        }

        li:nth-child(4) {
          &:hover {
            background: #ea558b;
          }
        }

        li:nth-child(4) {
          margin-right: 0px;
        }
      }
    }
  } // listbtn_wrap

  .cont_wrap {
    margin-top: 20px;
    width: 100%;
    // background: #ddd;
    height: 150px;
    overflow: hidden;

    .cont {
      border-radius: 20px;
      border: 1px solid #000;
      background: #eee;
      // display: inline-block;
      float: left;
      width: calc(100% / 3 - 20px);
      height: 100%;
      // background: beige;
      margin-right: 30px;
      position: relative;

      h3 {
        font-size: 2em;
        font-weight: bold;
        width: 220px;
        height: 90px;
        padding: 20px;
        display: inline-block;
        // background: yellow;
      }

      .newCheck {
        font-size: 2em;
        font-weight: bold;
        position: absolute;
        padding: 20px;
        right: 0;
        display: inline-block;
        // background-color: #20aa20;
      }

      .date {
        font-size: 1.6em;
        margin-top: 2px;
        padding: 20px;
        // background: palegreen;
      }
    }

    .cont:nth-child(3) {
      margin-right: 0px;
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    top: 450px;
    width: 100%;
  }
}
</style>
