<template>
  <div class="wrap">
    <div class="listbtn_wrap">
      <ul class="listbtn" v-for="list in list" :key="list">
        <a href="#">
          <li class="li_1">{{ list.listBtn[0] }}</li>
        </a>
        <a href="#">
          <li class="li_2">{{ list.listBtn[1] }}</li>
        </a>
        <a href="#">
          <li class="li_3">{{ list.listBtn[2] }}</li>
        </a>
        <a href="#">
          <li class="li_4">{{ list.listBtn[3] }}</li>
        </a>
      </ul>
    </div>

    <div class="newlist_wrap">
      <div class="newlist_cont" v-for="list in list" :key="list">
        <p>{{ list.newList[0] }}</p>
        <p>{{ list.newDate[0] }}</p>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          listBtn: ['새소식', '보도자료', '채용공고', '입찰공고'],
          newList: ['스미싱 사기 주의 안내', '2023년도 국민연금 기준소득월액 상,하한액 조정 안내', '2022년 우수 국민제안 심사위원회 결과 안내', '2023년 2분기 노후긴급자금 대부(실버론) 이자율 및 연체이자...', '2022년 제1차 국민연금 토론방 토론우수자 선정 및 기념품 당...'],
          newDate: ['2023-04-12', '2023-04-05', '2023-03-24', '2023-03-21', '2023-02-27'],
          broadList: ['[보도자료] 국민연금, 한국은행 350억달러 외환 스왑 한도 합의', '[보도해명자료] 4월 10일자 SBS BIZ 주식거래금지 관련', '[보도참고자료] 국민연금공단, 투명한 정보 공개로 우수공시기관...', '[보도자료] 국민연금 납부예외자는 "지역가입자 보험료지원" 신청하...', '[보조설명자료] 3월 28일자 이투데이 기사 관련'],
          broadDate: ['2023-04-13', '2023-04-10', '2023-04-07', '2023-04-05', '2023-03-28'],
          hireList: ['국민연금공단 공무직(사서직) 및 기간제 근로자(기록연구직, 고객...', '[국민연금공단 대구지역본부] 공무직(환경관리직) 공개 채용', '[국민연금공단 경인지역본부] 공무직(시설직) 공개 채용', '[국민연금공단 대전세종지역본부] 공무직(환경관리직, 시설직) 공개...', '[국민연금공단 부산지역본부] 공무직(시설직) 공개채용 공고'],
          hireDate: ['2023-04-12', '2023-04-10', '2023-04-10', '2023-04-06', '2023-04-06'],
          bidList: ['2023년 청풍리조트 사업장 생활계폐기물 처리 용역 단가 계약', '공익형 사옥 건립 타당성 조사 연구용역', '통계 소프트웨어 갱신(SAS)', '국민연금공단 서울남부지역본부 불용차량 매각 재공고', '2023년도 청풍리조트 전기안전관리자 위탁상주 용역 계약 공고'],
          bidDate: ['2023-04-17', '2023-04-13', '2023-04-12', '2023-04-11', '2023-04-11']
        }
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
  height: 300px;
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

      a {
        
        li {
          display: inline-block;
          width: 100px;
          height: 50px;
          border-radius: 25px;
          font-size: 1.6em;
          font-family: 'NanumBarunGothic';
          text-align: center;
          line-height: 55px;
          cursor: pointer;
          transition: .2s;
          // margin-right: 20px;
          // background-color: yellow;
          
          &:hover {
            color: #fff;
          }
        }

        .li_1 {
          &:hover {
            background: #ef681e;
          }
        }

        .li_2 {
          &:hover {
            background: #6992dd;
          }
        }

        .li_3 {
          &:hover {
            background: #20aa20;
          }
        }

        .li_4 {
          &:hover {
          background: #ea558b;
          }
        }

        li:nth-child(4) {
          margin-right: 0px;
        }
      }
    }
  }

  .newlist_wrap {
    // background-color: beige;
    // width: 200px;
    // height: 100px;

    .newlist_cont {
      width: calc(90% / 3);
      height: 200px;
      // background: yellow;
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