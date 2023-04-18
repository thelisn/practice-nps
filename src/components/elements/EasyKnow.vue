<template>
  <div class="wrap">
    <div class="easy_wrap">
      <h2>알기 쉬운 국민연금</h2>
      <div class="easy_innerwrap">
        <div class="easy_cont">
          <div class="box" v-for="cont in easy_box" :key="cont">
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
      easy_box: [
        {
          img: require("@/assets/images/easy_icon1.svg"),
          title: '국민연금제도'
        },
        {
          img: require("@/assets/images/easy_icon2.svg"),
          title: '가입유형'
        },
        {
          img: require("@/assets/images/easy_icon3.svg"),
          title: '사업장가입자'
        },
        {
          img: require("@/assets/images/easy_icon4.svg"),
          title: '지역가입자'
        },
        {
          img: require("@/assets/images/easy_icon5.svg"),
          title: '두루누리'
        },
        {
          img: require("@/assets/images/easy_icon6.svg"),
          title: '연금종류 및 청구'
        },
        {
          img: require("@/assets/images/easy_icon7.svg"),
          title: '연금보험료'
        },
        {
          img: require("@/assets/images/easy_icon8.svg"),
          title: '반환일시금 반납'
        },
        {
          img: require("@/assets/images/easy_icon9.svg"),
          title: '추후납부'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrap {
  position: relative;
  width: 1100px;
  margin: 0 auto;
  // top: 400px;
  // background: pink;

  .easy_wrap {
    position: absolute;
    top: -400px;
    right: 0;
    width: 525px;
    height: 400px;
    // background: whitesmoke;

    h2 {
      color: #ef681e;
      font-size: 2.6em;
      font-weight: bold;
    }

    .easy_innerwrap {
      width: 100%;
      height: 350px;
      margin-top: 25px;
      border: 1px solid #ffc5a3;
      border-radius: 30px;
      background: #fff;

      .easy_cont {
        width: 474px;
        height: 310px;
        margin: 0 auto;
        transform: translateY(15px);

        .box {
          display: inline-block;
          width: 150px;
          height: 100px;
          margin-right: 12px;
          margin-bottom: 10px;
          border-radius: 15px;
          transition: .3s;
          // background-color: pink;

          &:hover {
            background: #ffeee9
          }

          &:hover .img_box {
            background: #ef681e;

            .img {
              filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg) brightness(300%) contrast(102%);
            }
          }

          &:hover p {
            color: #ef681e;
            font-weight: 700;
          }

          .img_box {
            width: 46px;
            height: 46px;
            margin: 0 auto;
            border-radius: 23px;
            background: #eee;
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
    top: 150px;
    // background: pink;

    .easy_wrap {
      width: 430px;

      .easy_innerwrap {

        .easy_cont {
          width: 360px;
          height: 320px;

          .box {
            width: 110px;
            margin-right: 15px;

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
    top: 600px;
    width: 100%;
    // position: relative;
    // background: pink;

    .easy_wrap {
      position: relative;
      width: 90%;
      margin: 0 auto;
      // background: yellow;

      .easy_innerwrap {

        .easy_cont {
          width: 90%;

          .box {
            width: 26%;
            margin-right: 11%;

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