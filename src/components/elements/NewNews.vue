<template>
  <div class="wrap">
    <div class="listbtn_wrap">
      <ul class="listbtn">
        <a href="#" onclick="return false">
          <!-- onclick="return false"는 a태그 클릭 시 맨 위로 올라가는 기능 금지시키는 거 -->
          <button v-for="list in list" :key="list">{{ list.listCategory }}</button>
        </a>
      </ul>
    </div>

    <div class="cont_wrap">
      <a href="#">
      <div 
        class="cont" 
        v-for="(cont, contIndex) in list" 
        :key="`contIndex-${contIndex}`"
      >
        <div 
          class="data-repeat" 
          v-for="(contData, contDataIndex) in cont.data" 
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
              title: '국민연금 각종 신고 업무 핸드폰으로 쉽고 빠르게 하세요!',
              date: '2023-04-21',
              newCheck: false,
            },
            {
              title: '국민연금공단 세종사옥 신규 임대 안내',
              date: '2023-04-20',
              newCheck: false,
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
              title: '2022년 제1차 국민연금 토론방 토론우수자 선정 및 기념품 당첨자 결과 안내',
              date: '2023-02-27',
              newCheck: false,
            }
          ],
        }, // 새소식

        {
          listCategory: '보도자료',
          data: [
            {
              title: '[보도자료] 국민연금 노후준비 종합포털에서 별정우체국연금 조회도 가능해진다',
              date: '2023-04-21',
              newCheck: false,
            },
            {
              title: '[보도자료] 국민연금, 동반성장 평가 2년 연속 "최우수" 등급 달성!',
              date: '2023-04-21',
              newCheck: false,
            },
            {
              title: '[공동 보도설명자료] 4.19.(수) 연합뉴스 "이슈IN" 연 2천만원 공적연금 피부영자 탈락 보도 관련',
              date: '2023-04-20',
              newCheck: false,
            },
            {
              title: '[보도자료] 국민연금공단, "공공데이터 제공 운영실태 평가" 4년 연속 최고 등급인 "우수" 획득',
              date: '2023-04-20',
              newCheck: false,
            },
            {
              title: '[보도자료] BNY멜론 자산운용그룹, 전주사무소 개소 - 국민연금 업무 지원',
              date: '2023-04-19',
              newCheck: false,
            }
          ]
        }, // 보도자료

        {
          listCategory: '채용공고',
          data: [
            {
              title: '국민연금공단 체험형 청년인턴 추가 채용 공고',
              date: '2023-04-24',
              newCheck: true,
            },
            {
              title: '[국민연금공단 광주지역본부] 2023년도 공무직(보안직) 공개채용 공고',
              date: '2023-04-24',
              newCheck: true,
            },
            {
              title: '국민연금공단 공무직(사서직) 및 기간제 근로자(기록연구직, 고객센터상담직) 공개채용 공고',
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
            }
          ]
        }, // 채용공고

        {
          listCategory: '입찰공고',
          data: [
            {
              title: '2023년도 청풍리조트 전기안전관리자 위탁상주 용역 계약(재공고)',
              date: '2023-04-20',
              newCheck: false,
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
  width: 1100px;
  height: 220px;
  margin: 0 auto;
  // background: pink;

  .listbtn_wrap {
    width: 400px;
    height: 50px;
    border-radius: 25px;
    background: #eee;

    .listbtn {

      a {
    
        button {
          display: inline-block;
          width: 100px;
          height: 50px;
          border-radius: 25px;
          font-size: 1.6em;
          font-family: 'NanumSquareExtraBold';
          text-align: center;
          line-height: 55px;
          color: #585858;
          transition: .2s;
          cursor: pointer;
          // background-color: yellow;

          &:hover {
            color: #fff;
          }
        }

        button:nth-child(1) {
          &:hover {
            background: #ef681e;
          }
          &:focus {
            background: #ef681e;
            color: #fff;
          }
        }

        button:nth-child(2) {
          &:hover {
            background: #6992dd;
          }
          &:focus {
            background: #6992dd;
            color: #fff;
          }
        }

        button:nth-child(3) {
          &:hover {
            background: #20aa20;
          }
          &:focus {
            background: #20aa20;
            color: #fff;
          }
        }

        button:nth-child(4) {
          &:hover {
            background: #ea558b;
          }
          &:focus {
            background: #ea558b;
            color: #fff;
          }
        }

        button:nth-child(4) {
          margin-right: 0px;
        }
      }
    }
  } // listbtn_wrap

  .cont_wrap {
    overflow: hidden;
    width: 100%;
    height: 150px;
    margin-top: 20px;
    // background: #ddd;

    .cont {
      position: relative;
      float: left;
      width: calc(100% / 3 - 20px);
      height: 100%;
      margin-right: 30px;
      border-radius: 20px;
      background: #f8f8f8;
      // border: 0.7px solid #ef681e;
      // background: beige;

      h3 {
        display: -webkit-box;
        overflow: hidden;
        padding: 20px;
        width: 230px;
        height: 83px;
        color: #585858;
        font-size: 2em;
        font-family: 'NanumSquareBold';
        line-height: 30px;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
        word-break: break-all;
        text-overflow: ellipsis;
        // background: yellow;
        // font-weight: bold;
      }

      .newCheck {
        display: inline-block;
        position: absolute;
        top: 0;
        right: 0;
        padding: 20px;
        color: #ef681e;
        font-size: 2em;
        font-family: 'NanumSquareExtraBold';
        line-height: 30px;
        // font-weight: bold;
        // background-color: #20aa20;
      }

      .date {
        padding: 20px;
        margin-top: 2px;
        color: #585858;
        font-size: 1.6em;
        // background: palegreen;
        // font-weight: 300;
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
    width: 90%;
  }
}

@media screen and (max-width:950px) {
  .wrap {
    
    .listbtn_wrap {
      width: 300px;
      height: 40px;

      .listbtn {

        a {

          button {
            width: 75px;
            height: 40px;
            font-size: 1.4em;
            line-height: 43px;
            // background-color: pink;
          }
        }
      }
    }

    .cont_wrap {
      // background-color: pink;

      .cont {
        // margin-right: 20px;
        
        h3 {
          width: 130px;
          height: 75px;
          padding: 10px;
          font-size: 1.6em;
          line-height: 23px;
          -webkit-line-clamp: 3;
        }

        .newCheck {
          display: none;
        }

        .date {
          padding: 10px;
          margin-top: 35px;
          font-size: 1.3em;
        }
      }
    }
  }
}
</style>
