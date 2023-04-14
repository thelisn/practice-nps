<template>
<div class="service_wrap">
  <h2>자주 찾는 서비스</h2>
  <a href="#">
    <div class="box" v-for="cont in service_box" :key="cont">
      <p class="title">
        {{ cont.title }}
      </p>
      <div class="img_box">
        <div class="img">
          {{ cont.img }}
        </div>
      </div>
    </div>
  </a>
</div>
</template>

<script>
export default {
  data() {
    return {
      service_box: [
        {title: '내 연금 알아보기', img: '^오^'},
        {title: '지사 찾기', img: '^오^'},
        {title: '서식 찾기', img: '^오^'},
        {title: '4대 보험료 계산기', img: '^오^'},
        {title: '알기 쉬운 국민연금', img: '^오^'},
        {title: '웹 팩스 수신조회', img: '^오^'},
        {title: '국민연금 통계', img: '^오^'},
        {title: '채용 공고', img: '^오^'}
      ]
    }
  }
}

</script>

<style scoped lang="scss">
.service_wrap {
  position: absolute;
  right: 30px;
  z-index: -99;
  margin-top: 30px;
  width: 500px;
  height: 350px;
  border-radius: 30px;
  background: whitesmoke;
  // margin-left: 30px;
  
  h2 {
    padding: 40px;
    font-size: 2.6em;
    font-weight: bold;
    // background: pink;
  }

  a {
    display: inline-block;
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
        color: #fff;
      }
      
      .title {
        padding: 10px;
        color: #6a6a6a;
        font-size:1.6em;
        font-weight: 600;
        line-height: 17px;
        // background: pink;
      }
      
      .img_box {
        position: absolute;
        right: 8px;
        bottom: 8px;
        width: 30px;
        height: 30px;
        border-radius: 15px;
        background: #ddd;
        color: #6a6a6a;
        font-size: 1.2em;
        font-weight: 800;
        
        .img {
          text-align: center;
          top: 50%;
          transform: translateY(-50%);
          position: relative;
        }
      }
    }
  }
}

@media screen and (max-width:1080px) {
  .service_wrap {
    right: 0;
    width: 100%;
    height: 400px;
    border-radius: 0px;
    // margin-left: 0px;
    
    h2 {
      font-size: 3em;
    }

    a {
      margin-left: 3%;
      width: 100%;
      
      .box {
        width: 30%;
        height: 100px;
        margin-right: 2%;
      }
      
      .box:nth-child(3),
      .box:nth-child(6) {
        display: none;
      }
    }
  }
}
</style>