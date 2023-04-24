<template>
  <div class="wrap">
    <div class="service_wrap">
      <h2>자주 찾는 서비스</h2>
      <a href="#">
        <div class="box_wrap">
          <div class="box" v-for="cont in service_box" :key="cont">
            <p class="title">
              {{ cont.title }}
            </p>
            <div class="img_box">
              <div class="img">
                <img :src="cont.img" alt="아이콘">
              </div>
            </div>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      service_box: [
        {title: '내 연금 알아보기', img: require("@/assets/images/often_icon1.svg")},
        {title: '지사 찾기', img: require("@/assets/images/often_icon2.svg")},
        {title: '서식 찾기', img: require("@/assets/images/often_icon3.svg")},
        {title: '4대 보험료 계산기', img: require("@/assets/images/often_icon4.svg")},
        {title: '알기 쉬운 국민연금', img: require("@/assets/images/often_icon5.svg")},
        {title: '웹 팩스 수신조회', img: require("@/assets/images/often_icon6.svg")},
        {title: '국민연금 통계', img: require("@/assets/images/often_icon7.svg")},
        {title: '채용 공고', img: require("@/assets/images/often_icon8.svg")}
      ]
    }
  }
}

</script>

<style scoped lang="scss">

.wrap {
  width: 1100px;
  margin: 0 auto;
  
  .service_wrap {
    position: relative;
    margin-top: 30px;
    margin-left: 600px;
    width: 500px;
    height: 350px;
    border-radius: 30px;
    background: whitesmoke;
    // z-index: -99;
    // margin-right: 0px;
    // margin-left: 30px;
    
    h2 {
      padding: 40px;
      font-size: 2.6em;
      font-family: 'NanumSquareExtraBold';
      // font-weight: bold;
      // background: pink;
    }
    
    a {
      display: inline-block;
      width: 480px;
      margin-left: 20px;
      // background: pink;
      
      .box {
        position:relative;
        float: left;
        width: 100px;
        height: 90px;
        margin-right: 20px;
        margin-bottom: 20px;
        border: 1px solid #ccc;
        border-radius: 10px;
        background: white;
        transition: .1s;
        // display: inline-block;
        // position: absolute;
        // transform: translateX(25%);
        
        &:hover {
          border: 2px solid #28b4c9;
        }
      
        &:hover .title {
          color: #28b4c9;
        }

        &:hover .img_box{
          background: #28b4c9;
        }

        &:hover img {
          filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg) brightness(300%) contrast(102%);
        }
      
        .title {
          padding: 10px;
          color: #6a6a6a;
          font-size:1.7em;
          font-family: 'NanumSquareBold';
          line-height: 17px;
          // font-weight: 600;
          // background: pink;
        }
      
        .img_box {
          position: absolute;
          right: 8px;
          bottom: 8px;
          width: 30px;
          height: 30px;
          border-radius: 15px;
          background: #eee;
          // color: #6a6a6a;
          // font-size: 1.2em;
          // font-weight: 800;

          img {
            margin: 0 auto;
          }
        }
      }
    }
  }
}

@media screen and (max-width:1200px) {

  .wrap{
    width: 100%;
    
    .service_wrap {
      top: 400px;
      left: 0;
      width: 100%;
      height: 400px;
      margin-left: 0px;
      border-radius: 0px;
      // margin-left: 0px;
      
      h2 {
        font-size: 3em;
      }

      a {
        width: 100%;
        margin-left: 0px;
        // width: 830px;
        // margin-left: 3%;
        
        .box_wrap {
          position: absolute;
          width: 94%;
          margin-left: 3%;
          // background: green;
          .box {
            position: relative;
            width: 32%;
            height: 100px;
            margin-right: 2%;
          }

          .box:nth-child(4),
          .box:nth-child(8) {
            margin-right: 0px;
          }
      
          .box:nth-child(3),
          .box:nth-child(6) {
            display: none;
          }

          .box:nth-child(5),
          .box:nth-child(7),
          .box:nth-child(8) {
            margin-bottom: 0px;
          }
        }
      }
    }
  }
}
</style>