<template>
  <el-container class="container">
    <el-main class="main">
      <el-row :gutter="10" class="context-header">
        <el-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12">
          <div class="context-header-one">
            <span style="">完成</span>
          </div>
        </el-col>
        <el-col :xs="3" :sm="3" :md="3" :lg="3" :xl="3">
          <div class="context-header-two">
            <i class="el-icon-more"></i>
          </div>
        </el-col>
        <el-col :xs="3" :sm="3" :md="3" :lg="3" :xl="3">
          <div class="context-header-two">
            <i class="el-icon-map-location"></i>
          </div>
        </el-col>
        <el-col :xs="3" :sm="3" :md="3" :lg="3" :xl="3">
          <div class="context-header-two">
            <i class="el-icon-camera"></i>
          </div>
        </el-col>
        <el-col :xs="3" :sm="3" :md="3" :lg="3" :xl="3">
          <div class="context-header-two">
            <i class="el-icon-upload2"></i>
          </div>
        </el-col>
      </el-row>
      <div class="context-foot">
        <el-image
          src="https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg"
          fit="fit"></el-image>
        <el-row :gutter="5" class="foot-one">
          <el-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12" class="distance">
            <span class="distance-num">13.14</span><span>公里</span>
          </el-col>
          <el-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12" class="user-name">
            <span>菠萝-西门吹雪</span>
          </el-col>
        </el-row>
        <el-row :gutter="5" style="" class="foot-two">
          <el-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12" class="run">
            <span>咕咚 - 户外跑</span>
          </el-col>
          <el-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12" class="date">
            <i class="el-icon-partly-cloudy"></i> <span>6月26日 20:52</span>
          </el-col>
        </el-row>
        <!--进度条-->
        <div class="progress">
        </div>
        <div class="progress-text slow">
          <span>慢10‘19”</span>
        </div>
        <div class="progress-text fast">
          <span>9'05"快</span>
        </div>
        <el-row :gutter="80" class="foot-three">
          <el-col :xs="8" :sm="8" :md="8" :lg="8" :xl="8" class="three-col">
            <div style="" class="three-col-num">9'37"</div>
            <div class="three-col-unit speed">平均配速
            </div>
          </el-col>
          <el-col :xs="9" :sm="9" :md="9" :lg="9" :xl="9" class="three-col">
            <di style="font-size: 22px;font-weight: bold;" class="three-col-num">02:06:24</di>
            <div class="three-col-unit duration">时长</div>
          </el-col>
          <el-col :xs="7" :sm="7" :md="7" :lg="7" :xl="7" class="three-col">
            <div class="three-col-num">1032.1</div>
            <div class="three-col-unit calorie">千卡
            </div>
          </el-col>
        </el-row>
        <el-row :gutter="60" class="foot-four">
          <el-col :xs="8" :sm="8" :md="8" :lg="8" :xl="8" class="four-col">
            <div class="four-col-num step-num">18105</div>
            <div class="four-col-unit step-unit">
              步数
            </div>
          </el-col>
          <el-col :xs="9" :sm="9" :md="9" :lg="9" :xl="9" class="four-col">
            <div class="four-col-num step-fre">143
            </div>
            <div class="four-col-unit fre-unit">平均步频
            </div>
          </el-col>
          <el-col :xs="7" :sm="7" :md="7" :lg="7" :xl="7" class="four-col">
            <div class="four-col-num stride">72
            </div>
            <div class="four-col-unit stride-unit">平均步幅
            </div>
          </el-col>
        </el-row>
        <el-row :gutter="10" class="foot-five">
          <el-col :xs="22" :sm="6" :md="20" :lg="20" :xl="20">
            <el-button class="five-button" type="success" icon="el-icon-camera">发布动态
            </el-button>
          </el-col>
        </el-row>
      </div>
    </el-main>
  </el-container>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
  /*最外层容器*/
  .container {
    width: 100%;
    height: 100%;
    /*容器主体*/

    .main {
      width: 100%;
      height: 100%;
      padding: 0;

      /*顶部的五个图标*/

      .context-header {
        margin: 10px 10px auto 10px !important;

        /*完成按钮*/

        .context-header-one {
          width: 30%;
          height: 40px;
          background-color: #E5E9F2;
          border-radius: 20px 20px 20px 20px;
          display: flex;

          span {
            margin: auto;
            font-size: 14px;
          }
        }

        /*是个小图标*/

        .context-header-two {
          width: 100%;
          height: 40px;
          background-color: #E5E9F2;
          border-radius: 20px 20px 20px 20px;
          display: flex;

          i {
            margin: auto;
          }
        }
      }

      /*底部的内容*/

      .context-foot {
        margin: 387px auto 0 auto;
        background-color: #FFFFFF;
        width: 96%;
        height: 300px;
        position: relative;

        /*头像*/

        .el-image {
          width: 60px;
          height: 60px;
          border-radius: 50%;
          position: absolute;
          right: 10px;
          top: -30px;
        }

        /*第一行*/

        .foot-one {
          .distance {
            font-weight: bold;
            position: absolute;
            top: 20px;
            left: 10px;

            .distance-num {
              font-size: 30px;
            }
          }

          .user-name {
            position: absolute;
            top: 35px;
            right: -70px;
          }
        }

        /*第二行*/

        .foot-two {
          /*跑步方式*/

          .run {
            font-weight: bold;
            position: absolute;
            top: 55px;
            left: 15px;
          }

          /*日期*/

          .date {
            position: absolute;
            top: 55px;
            right: -60px;
          }
        }

        /*进度条*/

        .progress {
          position: absolute;
          top: 90px;
          width: 100%;
          height: 5px;
          border-radius: 10px 10px 10px 10px;
          background: -webkit-linear-gradient(left, #42CDA3, #3ACD77, #F0D23E, #EF7A4F, #E9664B);
        }

        /*进度条通用上的信息*/

        .progress-text {
          font-size: 12px;
          background-color: #FFFFFF;
          height: 10px;
          position: absolute;
          display: flex;

          span {
            margin: auto;
          }
        }

        /*慢的信息*/

        .slow {
          color: #42CDA3;
          width: 70px;
          top: 85px;
          left: 20px;
        }

        /*快的信息*/

        .fast {
          color: #E9664B;
          width: 50px;
          top: 85px;
          right: 20px;
        }

        /*第三行*/

        .foot-three {
          width: 100%;
          position: absolute;
          top: 110px;
          left: 25px;

          .three-col {
            position: relative;
            /*所有数字的样式*/

            .three-col-num {
              font-size: 22px;
              font-weight: bold;
            }

            /*所有单位的通用样式*/

            .three-col-unit {
              font-size: 16px;
              color: #CDCDCD;
              position: absolute;
            }

            /*公里数特有*/

            .speed {
              left: 30px;
            }

            /*时长特有*/

            .duration {
              left: 70px;
            }

            /*卡里路特有*/

            .calorie {
              left: 60px;
            }
          }
        }

        /*第四行*/

        .foot-four {
          width: 100%;
          position: absolute;
          top: 170px;
          left: 25px;

          .four-col {
            position: relative;
            /*数字通用*/

            .four-col-num {
              font-size: 22px;
              font-weight: bold;
            }

            /*步频数据特有*/

            .step-fre {
              position: absolute;
              right: 55px;
            }

            /*步幅数据特有*/

            .stride {
              position: absolute;
              right: -110px;
            }

            /*单位通用*/

            .four-col-unit {
              font-size: 16px;
              color: #CDCDCD;
              position: absolute;
            }

            /*步数单位特有*/

            .step-unit {
              left: 50px;
            }

            /*步频单位特有*/

            .fre-unit {
              left: 40px;
              top: 28px;
            }

            /*步幅单位特有*/

            .stride-unit {
              right: -130px;
              top: 28px;
            }
          }
        }

        /*第五行*/

        .foot-five {
          width: 100%;
          position: absolute;
          top: 230px;
          left: 20px;

          .five-button {
            width: 100%;
            height: 60px;
            background-color: #06C477;
            font-size: 20px;
          }
        }
      }
    }
  }
</style>
