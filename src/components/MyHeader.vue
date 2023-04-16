<template>
<div class="header_wrap">
  <div class="top_nav">
    <h1 class="logo">
      <a href="../App.vue"><img src="@/assets/images/logo.png" alt="NPS국민연금"></a>
    </h1>
  
    <div class="search_box">
      <input type="text" class="search_text">
      <input type="button" value="검색" class="search_btn">
    </div>
  
    <p class="login">
      <a href="#">전자민원이용(로그인필요)</a>
    </p>
  
    <div class="lang" id="lang">
      <button class="lang_btn" @click="show = !show">
        Language &#9660;
      </button>
      <div class="lang_list" v-if="show">
        <ul>
          <li v-for="lang in langs" :key="lang">{{ lang }}</li>
        </ul>
      </div>
    </div>
  </div>

  <div class="pc_gnb">
    <div class="pc_gnb_inner">
      <ul class="pc_gnb_list">
        <li class="pc_gnb_item">
          <a href="#">
          정보공개
        </a>
        <ul class="pc_gnb_list_depth2">
            <li>
              <a href="#" v-for="pc_gnb2_1 in pc_gnb2_1" :key="pc_gnb2_1">
                {{ pc_gnb2_1 }}
              </a>
            </li>
          </ul>
      </li>
        <li class="pc_gnb_item">
          <a href="#">전자민원</a>
          <ul class="pc_gnb_list_depth2">
            <li>
              <a href="#" v-for="pc_gnb2_2 in pc_gnb2_2" :key="pc_gnb2_2">
                {{ pc_gnb2_2 }}
              </a>
            </li>
          </ul>
        </li>
        <li class="pc_gnb_item">
          <a href="#">소통과 참여</a>
          <ul class="pc_gnb_list_depth2">
            <li>
              <a href="#" v-for="pc_gnb2_3 in pc_gnb2_3" :key="pc_gnb2_3">
                {{ pc_gnb2_3 }}
              </a>
            </li>
          </ul>
        </li>
        <li class="pc_gnb_item">
          <a href="#">연금소식</a>
          <ul class="pc_gnb_list_depth2">
            <li>
              <a href="#" v-for="pc_gnb2_4 in pc_gnb2_4" :key="pc_gnb2_4">
                {{ pc_gnb2_4 }}
              </a>
            </li>
          </ul>
        </li>
        <li class="pc_gnb_item">
          <a href="#">연금정보</a>
          <ul class="pc_gnb_list_depth2">
            <li>
              <a href="#" v-for="pc_gnb2_5 in pc_gnb2_5" :key="pc_gnb2_5">
                {{ pc_gnb2_5 }}
              </a>
            </li>
          </ul>
        </li>
        <li class="pc_gnb_item">
          <a href="#">공단소개</a>
          <ul class="pc_gnb_list_depth2">
            <li>
              <a href="#" v-for="pc_gnb2_6 in pc_gnb2_6" :key="pc_gnb2_6">
                {{ pc_gnb2_6 }}
              </a>
            </li>
          </ul>
        </li>
      </ul>

      <!-- <ul class="pc_gnb_list">
        <li class="pc_gnb_item">
          <a href="#" v-for="pc_gnb_item in pc_gnb" :key="pc_gnb_item">
            {{ pc_gnb_item }}
          </a>
        </li>
      </ul> -->

      <div class="all_menu">
        <a href="#">
          <p>전체메뉴</p>
          <div class="ham_btn">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </a>
      </div>
    </div>
  </div>
  
  </div> <!-- header wrap end -->
</template>

<script>

export default {
  data() {
    return {
      langs: ['English', '中国', 'Thailand', 'Indonesia', 'Mongolia'],

      show: false, //lang toggle

      // pc_gnb: ['정보공개', '전자민원', '소통과 참여', '연금소식', '연금정보', '공단소개'],
      pc_gnb2_1: ['사전정보공표', '정보목록', '정보공개', '공공데이터개방', '자료실', '사업실명제', '공시송달'],
      pc_gnb2_2: ['개인민원', '사업장민원', '국민연금EDI', '웹팩스 수신조회', '지사/직원찾기', '서식 찾기', '인터넷 납부'],
      pc_gnb2_3: ['고객상담실', '친절/불친절', '국민제안', '국민연금 토론방', '국민의소리 반영함', '신고센터', '국민연금자문단', '고객서비스 헌장', '정보화사업', '규제혁신', '안전신문고', 'NPS기업성장응답센터'],
      pc_gnb2_4: ['새소식', '보도자료', '채용안내', '제5차 재정계산', '입찰정보', '지사/센터소식', '사옥임대 및 시설개방'],
      pc_gnb2_5: ['알기쉬운 국민연금', '국민연금통계', '세계의연금제도', '사회보장협정', '법령 및 사규(제규정)', '자료실'],
      pc_gnb2_6: ['이사장', '비전 및 전략', '경영진', '연혁 및 CI', '조직 및 인원', '이사회', '경영공시', '공단견학']
    }
  }
}
</script>

<style scoped lang="scss">
.header_wrap {
  // background-color: pink;

  .top_nav {
    position: relative;
    width: 90%;
    height: 88px;
    margin: 0 auto;
    // background-color: salmon;
    
    .logo {
      position: relative;
      top: 50%;
      width: 204px;
      height: 48px;
      transform: translateY(-50%);
      // background-color: pink;
      
      img {
        width:100%;
      }
    }
    
    .search_box {
      position: absolute;
      top: 20%;
      left:50%;
      width: 180px;
      // background: yellow;
      
      .search_text {
        width: 100%;
        height: 34px;
        border: 1px solid #ccc;
        border-radius: 30px;
      }
      
      .search_btn {
        position:absolute;
        top:8px;
        right: 10px;
        width: 16px;
        height:16px;
        border: none;
        background: url(@/assets/images/search.svg) no-repeat center/cover;
        text-indent: -9999px;
        cursor: pointer;
        // background-color: seagreen;
      }
    } // search_box

    .login {
      position: absolute;
      top: 30%;
      left: 70%;
      font-size: 1.7em;

      a {
        color: #777;

        &:hover {
          font-weight: 500;
          // border-bottom: 1px solid #777;
          // color: #000;
        }
      }
    }

    .lang {
      display: inline-block;
      position: absolute;
      top: 26%;
      right: 3%;
      z-index: 999;

      .lang_btn {
        margin-bottom: 10px;
        font-size: 1.7em;
        color: #777;
      }

      .lang_list {
        background: white;
        font-size: 1.7em;
        color: #777;
        box-shadow: 0 2px 3px 0 rgba(0, 0, 0, 0.2);
        // display: none;
        // 일단 display: none 해놓음
        
        li {
          position:relative;
          padding: 7px;
          cursor: pointer;

          &:hover {
            color: #7494ce;
            font-weight: 600;
          }
        }
      }
    }
  } // top_nav

  .pc_gnb {
    width: 100%;
    height: 60px;
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;
    
    .pc_gnb_inner {
      position: relative;
      width:90%;
      margin: 0 auto;
      z-index: 99;

      .pc_gnb_list {
        display: inline-block;
        width: 100%;
        margin-right: 100px;

        >li {
          position: absolute;
          top: 0px;
          width:100%;
          height: 58px;
          // background-color: cornflowerblue;
        }

        >li:nth-child(2) {
          margin-left: calc(90% / 6);
        }

        >li:nth-child(3) {
          margin-left: calc(90% / 3);
        }

        >li:nth-child(4) {
          margin-left: calc(90% / 2);
        }

        >li:nth-child(5) {
          margin-left: calc(90% / 1.5);
        }

        >li:nth-child(6) {
          margin-left: calc(90% / 1.2);
        }
        
        .pc_gnb_item {
          
          >a {
            display: inline-block;
            width: calc(90% / 6);
            font-size: 2.2em;
            color: #6a6a6a;
            font-weight: bold;
            line-height: 58px;
            text-align: center;
            // background: yellow;
            // opacity: .7;
            
            &:hover {
            color: #5b7dbb;
            }
          
            &:hover + .pc_gnb_list_depth2 {
              display: block;
            }
          }

          .pc_gnb_list_depth2 {
            display: none;
            width: calc(90% / 6);
            margin-top: 1px;
            border-radius: 20px;
            background: #fff;
            box-shadow: 2px 5px 10px #ccc;
            // height: 700px;
            // background: whitesmoke;

            &:hover {
              display: block;
            }
            
            a{
              display: block;
              color:#6a6a6a;
              font-size: 1.9em;
              font-weight: 500;
              line-height: 58px;
              text-align: center;
              // width: calc(90% / 6);

              &:hover {
                color: #5b7dbb;
              }
            }
          }
        }
      } // pc_gnb_list

      .all_menu {
        position: absolute;
        right: 20px;
        font-size: 2.2em;
        font-weight: bold;
        // background-color: pink;
        
        a {
          position: relative;
          top: 8px;
          color: #6a6a6a;
        }
        
        .ham_btn {
          display: inline-block;
          position: absolute;
          top: 0;
          left: 100%;
          width: 20px;
          height: 16px;
          margin-left: 6px;
          // background-color: pink;
          
          span {
            display: block;
            width:20px;
            height:2px;
            margin-bottom: 6px;
            background: #6a6a6a;
          }
        }
      }
    }
  }
} // header_wrap

@media screen and (max-width: 1200px) {
  .header_wrap {
    // background: pink;

    .top_nav {
      // background-color: yellow;

      .logo {
        width: 190px;
        margin: 0 auto;
        transform: translateY(-40%);
        // left: 50%;
        // transform: translateX(-50%);
      }

      .search_box,
      .login,
      .lang {
        display: none;
      }
    } // top_nav

    .pc_gnb {
      border: none;
      background-color: green;
      height: 0;

      .pc_gnb_inner {

        .pc_gnb_list {
          display: none;
        }

        .all_menu {

          a {

            p {
              display: none;
            }

            .ham_btn {
              margin-top: -65px;
              margin-left: -15px;
              // background-color: pink;
              
              span {
                width: 25px;
                height: 3px;
                margin-bottom: 7px;
              }
            }
          }
        }
      }
    }
  }
}

</style>