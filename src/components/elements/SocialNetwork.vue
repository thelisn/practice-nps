<template>
  <div class="wrap">
    <div class="sns_wrap">
      <h2>사회관계망 서비스</h2>
      <div class="sns_innerwrap">
        <div class="sns_btn">
          <button v-for="item in btn" :key="item">
            <img :src="item.img" alt="sns아이콘">
            <p>{{ item.name }}</p>
          </button>
        </div>
        <div class="sns_cont">
          <a href="#">
            <div class="box" v-for="cont in sns" :key="cont">
              <div class="img">
                <img :src="cont.img" alt="사회관계망 서비스">
              </div>
              <div class="text">
                <p class="title">{{ cont.title }}</p>
                <p class="desc">{{ cont.desc }}</p>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      btn: [
        {
          img: require("@/assets/images/sns_icon1.svg"),
          name: '온에어'
        },
        {
          img: require("@/assets/images/sns_icon2.svg"),
          name: '블로그'
        },
        {
          img: require("@/assets/images/sns_icon3.svg"),
          name: '유튜브'
        },
        {
          img: require("@/assets/images/sns_icon4.svg"),
          name: '인스타그램'
        }
      ],
      sns: [
        {
          img: require("@/assets/images/sns_icon1.svg"),
          title: '국민연금 온에어',
          desc: '한 눈에 확인하는 국민연금 SNS콘텐츠'
        },
        {
          img: require("@/assets/images/sns_icon2.svg"),
          title: '국민연금공단 블로그',
          desc: '쉽게 보는 국민연금제도 100% 활용법'
        },
        {
          img: require("@/assets/images/sns_icon3.svg"),
          title: '국민연금공단 유튜브', 
          desc: '영상으로 생생하게 만나는 국민연금'
        },
        {
          img: require("@/assets/images/sns_icon4.svg"),
          title: '국민연금공단 인스타그램',
          desc: '연대리가 소개하는 국민연금 일상'
        }
      ]
    }
  }
}

</script>

<style scoped lang="scss">
.wrap {
  width: 1100px;
  height: 250px;
  margin: 0 auto;
  // background: cornflowerblue;
  transform: translateY(350px);
  
  .sns_wrap {
    position: absolute;
    right: 0;
    width: 500px;
    height: 100%;
    // height: 250px;
    // background: yellow;

    h2 {
      font-size: 2.6em;
      font-weight: bold;
      // color: #000;
    }

    .sns_innerwrap {

      .sns_btn {
        display: none; // 이거 수정해야함!!!!!
        // width: 100px;
        // height: 100px;
        // margin-left: 500px;
        // background: green;
        // // display: inline-block;
      }

      .sns_cont {

        a {

          .box {
            position: absolute;
            width: 100%;
            height: 200px;
            border-radius: 30px;
            bottom: 0;
            // opacity: .2;

            img {
              position: absolute;
              top: 50%;
              transform: translateY(-50%);
              left: 20px;
              // background: pink;
            }

            .text {
              display: inline-block;
              position: relative;
              top: 65px;
              margin-left: 140px;
              // background: beige;
              
              p {
                color: #fff;
              }

              .title {
                font-size: 3.4em;
                font-weight: 600;
                margin-bottom: 15px;
              }

              .desc {
                font-size: 2.3em;
              }
            }
          }

          .box:nth-child(1) {
            background: #4e92d6;
          }

          .box:nth-child(2) {
            background: #239a31;
          }

          .box:nth-child(3) {
            background: #cb4343;
          }

          .box:nth-child(4) {
            background: linear-gradient(to right, #fed446, #fa984b, #fe535c, #ea4cc5, #ab5cf0);
          }
        }
      }
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: 100%;
    // background: pink;

    .sns_wrap {
      position: relative;
      width: 90%;
      margin: 0 auto;

      .sns_innerwrap {

        .sns_cont {

          a {

            .box {

              .text {

                .title {
                  font-size: 3em;
                  margin-bottom: 12px;
                }

                .desc {
                  font-size: 2em;
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>