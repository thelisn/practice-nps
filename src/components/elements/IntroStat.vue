<template>
  <div class="wrap">
    <div class="intro_wrap">
      <h2>공단소개 및 통계</h2>
      <div class="intro_innerwrap">
        <div class="intro_cont">
          <div class="box" v-for="cont in intro_box" :key="cont">
            <a href="#">
              <div class="img_box">
                <div class="img">
                  <img :src="cont.img" alt="아이콘">
                </div>
              </div>
              <p class="title">
                {{ cont.title }}
              </p>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      intro_box: [
        {
          img: require("@/assets/images/intro_icon1.svg"),
          title: '연혁 및 CI'
        },
        {
          img: require("@/assets/images/intro_icon2.svg"),
          title: '조직 및 인원'
        },
        {
          img: require("@/assets/images/intro_icon3.svg"),
          title: '경영공시'
        },
        {
          img: require("@/assets/images/intro_icon4.svg"),
          title: '지사찾기'
        },
        {
          img: require("@/assets/images/intro_icon5.svg"),
          title: '비전 및 전략'
        },
        {
          img: require("@/assets/images/intro_icon6.svg"),
          title: '가입 및 급여통계'
        },
        {
          img: require("@/assets/images/intro_icon7.svg"),
          title: '기금운용통계'
        },
        {
          img: require("@/assets/images/intro_icon8.svg"),
          title: '전국연금지급통계'
        },
        {
          img: require("@/assets/images/intro_icon9.svg"),
          title: '연금수급자 기네스'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  position: relative;
  top: 400px;
  width: 1100px;
  margin: 0 auto;
  // height: 1000px;
  // background: pink;

  .intro_wrap {
    width: 525px;
    height: 400px;
    // background: whitesmoke;

    h2 {
      color: #6992dd;
      font-size: 2.6em;
      font-weight: bold;
      // padding: 20px;
      // background: beige;
    }

    .intro_innerwrap {
      width: 100%;
      height: 350px;
      margin-top: 25px;
      border: 1px solid #c9deff;
      border-radius: 30px;
      background: #fff;
      // position: absolute;
      // bottom: 0;

      .intro_cont {
        width: 474px;
        height: 310px;
        margin: 0 auto;
        transform: translateY(15px);
        // background: yellow;

        .box {
          display: inline-block;
          width: 150px;
          height: 100px;
          margin-right: 12px;
          margin-bottom: 10px;
          border-radius: 15px;
          transition: .3s;
          // background-color: #dbebff;

          &:hover {
            background: #f2f7ff;
          }

          &:hover .img_box {
            background: #6992dd;

            .img {
              filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg) brightness(300%) contrast(102%);
            }
          }

          &:hover p {
            color: #517ed3;
            font-weight: 700;
          }

          .img_box {
            width: 46px;
            height: 46px;
            margin: 0 auto;
            background: #eee;
            border-radius: 23px;
            transform: translateY(12px);
            transition: .3s;
          }

          p {
            margin-top: 23px;
            color: #6a6a6a;
            font-size: 1.6em;
            font-weight: 500;
            text-align: center;
          }
        }
        
        .box:nth-child(3n) {
          margin-right: 0px;
        }
      }
    }
  }
}

@media screen and (max-width:1200px) {
  .wrap {
    width: 900px;
    // background: pink;

    .intro_wrap {
      width: 430px;

      .intro_innerwrap {
        
        .intro_cont {
          width: 360px;
          height: 320px;
          // background: yellow;

          .box {
            width: 110px;
            margin-right: 15px;
            // margin-bottom: 20px;
            // background-color: pink;

            .img_box {
              width: 40px;
              height: 40px;

              .img {

                img {
                  width: 40px;
                }
              }
            }

            p {
              margin-top: 28px;
              font-size: 1.5em;
            }
          }
        }
      }
    }
  }
}

@media screen and (max-width:950px) {
  .wrap {
    width: 100%;
    // background: pink;

    .intro_wrap {
      width: 90%;
      margin: 0 auto;
      // background-color: yellow;

      .intro_innerwrap {

        .intro_cont {
          width: 90%;
          // background-color: gray;
          
          .box {
            width: 26%;
            margin-right: 11%;
            // background: pink;

            .img_box {
              width: 52px;
              height: 52px;
              border-radius: 26px;

              .img {
                
                img {
                  width: 52px;
                }
              }
            }

            p {
              margin-top: 22px;
              font-size: 1.5em;
            }
          }
        }
      }
    }
  }
}
</style>