<template>
<div class="service_wrap">
  
  <div class="personal_service_wrap active">
    <h2>개인 서비스</h2>
    <a href="#">
      <div class="personal_service_box" v-for="personal in personal" :key="personal">
        <p v-html="personal"></p>
      </div>
      <div class="personal_btn">
        <p>&rarr;</p>
      </div>
    </a>
  </div>
  
  <div class="business_service_wrap active">
    <h2>사업장 서비스</h2>
    <a href="#">
      <div class="business_service_box" v-for="business in business" :key="business">
        <p v-html="business"></p>
      </div>
      <div class="business_btn">
        <p>&larr;</p>
      </div>
    </a>
  </div>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      personal: ['가입증명서<br>발급', '가입내역<br>조회', '보험료<br>결정내역 조회', '연금산정용가입<br>내역확인서 발급', '연금 / 일시금<br>청구', '전화번호 /<br>이메일 변경'],
      business: ['국민연금 EDI', '보험료 부과내역<br>증명서 발급', '사업장 가입자<br>증명서 발급', '사업장 보험료<br>지원내역 조회', '사업장 관리번호<br>조회', '사업장 가입자<br>명부 조회']
    }
  }
}
</script>

<style scoped lang="scss">

.service_wrap {
  position: absolute;
  top: 560px;
  left: 50%;
  width: 96%;
  height: 220px;
  transform: translateX(-50%);
  // top: 50%;
  // background: pink;
  
  .personal_service_wrap {
    width: 78%;
    height: 100%;
    background: #d5f7fc;
    border-radius: 25px;
    
    h2 {
      padding: 30px;
      color: #158799;
      font-size: 2.6em;
      font-weight: bold;
    }
    
    a {
      .personal_service_box {
        float: left;
        width: calc(75% / 6);
        height: 80px;
        margin-top: 10px;
        margin-right: 1%;
        margin-left: 18px;
        border-radius: 25px;
        background: white;
        transition: .3s;
        // display: inline-block;
        
        p {
          margin-top: 20%;
          color: #158799;
          font-size: 1.5em;
          font-weight: 500;
          text-align: center;
          line-height: 20px;
        }
        
        &:hover {
          background: #158799;
        }

        &:hover p {
          color: #fff;
        }
      }

      .personal_service_box:nth-child(6) {
        margin-right: 0px;
      }

      .personal_btn {
        display: none;
      }
    }
  }

  .personal_service_wrap.active {
    width: 220px;
    height: 220px;
    
    h2 {
      position: relative;
      top: 50%;
      padding: 50px;
      transform: translateY(-50%);
      // background: yellow;
    }

    .personal_service_box {
      display: none;
    }

    .personal_btn {
        display: block;
        position: absolute;
        top: 50%;
        left: 180px;
        width: 80px;
        height: 80px;
        border-radius: 40px;
        background: #d5f7fc;
        transform: translateY(-50%);
        // background-color: yellow;
        
        p {
          margin-left: 6px;
          padding: 28px;
          color: #158799;
          font-size: 3em;
          // background-color: yellow;
        }
      }
    }
    
    .business_service_wrap {
      position: absolute;
      top: 0;
      right: 0;
      width: 220px;
      height: 220px;
      border-radius: 25px;
      background:#ffe5d1;
      
      h2 {
        position: relative;
        top: 50%;
        padding: 40px;
        color: #d66000;
        font-size: 2.6em;
        font-weight: bold;
        transform: translateY(-50%);
      }
      
      a {
        .business_service_box {
          display: none;
      }

      .business_btn {
        position: absolute;
        top:50%;
        right: 180px;
        width: 80px;
        height: 80px;
        border-radius: 40px;
        background: #ffd4b4;
        transform: translateY(-50%);
        // background-color: yellow;
        
        p {
          color: #d66000;
          font-size: 3em;
          padding: 28px;
          margin-left: -6px;
        }
      }
    }
  }

  .business_service_wrap.active {
    width: 78%;
    height: 100%;
    z-index: -9;
    
    h2 {
      top: 0px;
      padding: 50px;
      transform: translateY(0);
      // position: relative;
      // background: yellow;
    }

    a{
      .business_service_box {
        display: block;
        float: left;
        width: calc(75% / 6);
        height: 80px;
        margin-top: -30px;
        margin-right: 1%;
        margin-left: 18px;
        border-radius: 25px;
        background: white;
        transform: translateX(40px);
        transition: .3s;
        // margin-top: 10px;
        
        p {
          margin-top: 20%;
          color: #d66000;
          font-size: 1.5em;
          font-weight: 500;
          line-height: 20px;
          text-align: center;
        }
        
        &:hover {
          background: #d66000;
        }
        
        &:hover p {
          color: #fff;
        }
      }
      
      .business_service_box:nth-child(1) p {
        margin-top: 31%;
      }
      
      .business_btn {
        display: none;
      }
    }
  }
}

@media screen and (max-width:1080px) {
  .service_wrap {
    display: none;
  }
}
</style>