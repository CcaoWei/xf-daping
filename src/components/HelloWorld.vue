<template>
  <dv-full-screen-container class="datav-content">
    <el-row type="flex" :gutter="50" class="row-bg all-row">
      <el-col :span="12">
        <div class="grid-content">
          <el-row type="flex" :gutter="20" class="row-bg all-row">
            <el-col :span="12" class="dp-flex">
              <div class="bg-purple">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:10px ">项目穿越类型统计</div>
                  <div class="xm-style" ref="dvActiveChart">
                    <dv-active-ring-chart :config="config" :style="{width:dvActiveChartW,height:'150px'}" />
                    <div>
                      <div class="xm-style mb3 dp-border"><span class="dot C90A55"></span>&nbsp;<span style="color: #C90A55;font-size:12px">一类事件&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> <span style="color: #fff;font-size:12px">9999</span> </div>
                      <div class="xm-style mb3 dp-border"><span class="dot CBFD"></span>&nbsp;<span style="color: #45CBFD;font-size:12px">二类事件&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> <span style="color: #fff;font-size:12px">9999</span></div>
                      <div class="xm-style mb3 dp-border"><span class="dot F7EFF"></span>&nbsp;<span style="color: #6F7EFF;font-size:12px">三类事件&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> <span style="color: #fff;font-size:12px">9999</span></div>
                      <div class="xm-style mb3 dp-border"><span class="dot C545FE"></span>&nbsp;<span style="color: #C545FE;font-size:12px">其他&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> <span style="color: #fff;font-size:12px">9999</span></div>
                    </div>

                  </div>

                </dv-border-box-1>
              </div>
              <div class="bg-purple" ref="dvWaterPond">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:20px ">北京市分区的工程数量</div>
                  <div class="xm-style pd15 pr20">
                    <div style="margin-right:10px">

                      <dv-water-level-pond :config="WaterLevelPond" style="width:130px;height:130px" />
                      <div style="color:#447696;">总办结率</div>
                    </div>
                    <div class="xm-style" style="justify-content: space-between;padding:0 15px">

                      <div style="font-size:12px;color:#7587C2">
                        <div class="mb3">株洲市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                        <div class="mb3">南充市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                        <div class="mb3">上海市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                        <div class="mb3">吴忠市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                      </div>

                      <div style="font-size:12px;color:#7587C2">
                        <div class="mb3">北京市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                        <div class="mb3">厦门市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                        <div class="mb3">天水市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                        <div class="mb3">焦作市&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#fff">50.01%</span></div>
                      </div>

                    </div>
                  </div>

                  <!-- <dv-water-level-pond :config="WaterLevelPond" :style="{width:dvWaterPondW,height:'150px'}" /> -->
                </dv-border-box-1>
              </div>
            </el-col>
            <el-col :span="12">
              <div class="grid-content" ref="dvCapsule">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:20px ">1到16号线的工程数目</div>
                  <div class="xm-style" style="justify-content: space-between;padding:0 25%;box-sizing:border-box;margin-bottom:20px ">
                    <div style="font-size:14px;color:#7587C2"><span style="font-size:22px;color:#4EE8F9;font-weight:600">7</span>&nbsp;&nbsp;事件类型</div>
                    <div style="font-size:14px;color:#7587C2"><span style="font-size:22px;color:#4EE8F9;font-weight:600">127</span>&nbsp;&nbsp;事件总数</div>
                  </div>
                  <dv-capsule-chart :config="dvCapsule" :style="{width:dvCapsuleW,height:dvCapsuleH}" style="padding:0 30px" />
                </dv-border-box-1>
              </div>
            </el-col>
          </el-row>

        </div>
      </el-col>
      <el-col :span="12">
        <div class="grid-content">
          <el-row type="flex" :gutter="20" class="row-bg all-row">
            <el-col :span="12" class="dp-flex">
              <div class="bg-purple">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:20px ">日报上传数量</div>
                  <div class="map1" id="map1"></div>
                </dv-border-box-1>
              </div>
              <div class="bg-purple">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:20px ">监测单位项目情况</div>
                  <div class="map2" id="map2"></div>

                </dv-border-box-1>
              </div>
            </el-col>
            <el-col :span="12" class="dp-flex">
              <div class="h40">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:20px ">工程数量（竣工、新建、在施）</div>
                  <div class="xm-style" style="justify-content: space-around;padding:0 15px;box-sizing:border-box">
                    <div>
                      <div><img width="60" src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png" alt=""></div>
                      <div style="font-size:14px;color:#899ACB">为民服务活动</div>
                      <div style="font-size:24px;color:#4BE3EA;font-weight:600">19</div>
                    </div>
                    <div>
                      <div><img width="60" src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png" alt=""></div>
                      <div style="font-size:14px;color:#899ACB">服务人员</div>
                      <div style="font-size:24px;color:#4BE3EA;font-weight:600">312</div>
                    </div>
                    <div>
                      <div><img width="60" src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png" alt=""></div>

                      <div style="font-size:14px;color:#899ACB">服务团队</div>
                      <div style="font-size:24px;color:#4BE3EA;font-weight:600">1901</div>
                    </div>
                  </div>
                </dv-border-box-1>
              </div>
              <div class="h56" ref="dvScroll">
                <dv-border-box-1>
                  <div style="padding-top:10px;margin-bottom:20px ">滚动显示数据上传</div>
                  <dv-scroll-board :config="dvScroll" :style="{width:dvScrollW,height:dvScrollH,padding:'0 20px',boxSizing: 'border-box',fontSize:'12px'}" />
                </dv-border-box-1>
              </div>
            </el-col>
          </el-row>
        </div>
      </el-col>
    </el-row>

  </dv-full-screen-container>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      config: {
        radius: "80%",
        activeRadius: "84%",
        data: [
          {
            name: "一类事件",
            value: 1334,
          },
          {
            name: "二类事件",
            value: 409,
          },
          {
            name: "三类事件",
            value: 1973,
          },
          {
            name: "其他",
            value: 1377,
          },
        ],
        digitalFlopStyle: {
          fontSize: 12,
        },
        color: ["#C90A55", "#45CBFD", "#6F7EFF", "#C545FE"],
        showOriginValue: true,
      },
      WaterLevelPond: {
        data: [55],
        shape: "round",
      },
      dvCapsule: {
        data: [
          {
            name: "南阳",
            value: 167,
          },
          {
            name: "周口",
            value: 123,
          },
          {
            name: "漯河",
            value: 98,
          },
          {
            name: "郑州",
            value: 75,
          },
          {
            name: "西峡",
            value: 66,
          },
        ],
        colors: ["#e062ae", "#fb7293", "#e690d1", "#32c5e9", "#96bfff"],
        unit: "单位",
        showValue: true,
      },
      dvActiveChartW: "140px",
      dvActiveChartH: "140px",
      dvWaterPondW: "140px",
      dvWaterPondH: "140px",
      dvCapsuleH: "140px",
      dvCapsuleW: "140px",
      dvScrollH: "140px",
      dvScrollW: "140px",
      map1: {
        xAxis: {
          type: "category",
          boundaryGap: false,
          data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"],
          axisLine: {
            onZero: false,
            lineStyle: {
              color: "#fff",
            },
          },
        },
        yAxis: {
          type: "value",
          axisLine: {
            onZero: false,
            lineStyle: {
              color: "#fff",
            },
          },
        },
        series: [
          {
            data: [120, 190, 230, 220, 232, 201, 134],
            type: "line",
            areaStyle: {
              color: {
                type: "linear",
                x: 0,
                y: 0,
                x2: 0,
                y2: 1,
                colorStops: [
                  {
                    offset: 0,
                    color: "#79DBE2", // 0% 处的颜色
                  },
                  {
                    offset: 1,
                    color: "#0B295B", // 100% 处的颜色
                  },
                ],
                global: false, // 缺省为 false
              },
            },
            itemStyle: {
              normal: {
                color: "#2F92AB", //折点颜色
                lineStyle: {
                  color: "#2F92AB", //折线颜色
                },
              },
            },
          },
        ],
      },
      map2: {
        legend: {
          textStyle: {
            color: "#fff",
          },
        },
        tooltip: {},
        dataset: {
          source: [
            ["product", "2015", "2016", "2017"],
            ["Matcha Latte", 43.3, 85.8, 93.7],
            ["Milk Tea", 83.1, 73.4, 55.1],
            ["Cheese Cocoa", 86.4, 65.2, 82.5],
            ["Walnut Brownie", 72.4, 53.9, 39.1],
          ],
        },
        xAxis: {
          type: "category",
          axisLine: {
            onZero: false,
            lineStyle: {
              color: "#fff",
            },
          },
        },
        yAxis: {
          axisLine: {
            onZero: false,
            lineStyle: {
              color: "#fff",
            },
          },
        },
        // Declare several bar series, each will be mapped
        // to a column of dataset.source by default.
        series: [
          {
            type: "bar",
            itemStyle: {
              // color: "#BD3CFA",
              color: new this.$echarts.graphic.LinearGradient(0, 0, 0, 1, [
                { offset: 0, color: "#6F088D" },
                { offset: 0.5, color: "#9C2CC4" },
                { offset: 1, color: "#BD3CFA" },
              ]),
            },
          },
          {
            type: "bar",
            itemStyle: {
              // color: "#43C6F5",
              color: new this.$echarts.graphic.LinearGradient(0, 0, 0, 1, [
                { offset: 0, color: "#19459E" },
                { offset: 0.5, color: "#3395D9" },
                { offset: 1, color: "#43C6F5" },
              ]),
            },
          },
        ],
      },
      dvScroll: {
        header: ["地址", "时间", "涉事人员"],
        headerBGC: "#122060",
        oddRowBGC: "",
        evenRowBGC: "",
        headerHeight: "30",
        align: ["center"],
        data: [
          ["行1列1", "行1列2", "行1列3"],
          ["行2列1", "行2列2", "行2列3"],
          ["行3列1", "行3列2", "行3列3"],
          ["行4列1", "行4列2", "行4列3"],
          ["行5列1", "行5列2", "行5列3"],
          ["行6列1", "行6列2", "行6列3"],
          ["行7列1", "行7列2", "行7列3"],
          ["行8列1", "行8列2", "行8列3"],
          ["行9列1", "行9列2", "行9列3"],
          ["行10列1", "行10列2", "行10列3"],
        ],
      },
    };
  },
  mounted() {
    this.$nextTick(function () {
      setTimeout(() => {
        this.dvActiveChartW = `${this.$refs.dvActiveChart.clientWidth / 2}px`;
        this.dvActiveChartH = `${this.$refs.dvActiveChart.clientHeight}px`;
        this.dvWaterPondW = `${this.$refs.dvWaterPond.clientWidth / 2}px`;
        this.dvWaterPondH = `${this.$refs.dvWaterPond.clientHeight / 2}px`;
        this.dvCapsuleW = `${this.$refs.dvCapsule.clientWidth - 10}px`;
        this.dvCapsuleH = `${this.$refs.dvCapsule.clientHeight - 120}px`;
        this.dvScrollH = `${this.$refs.dvScroll.clientHeight - 80}px`;
        this.dvScrollW = `${this.$refs.dvScroll.clientWidth}px`;
        this.drawer();
        this.drawer2();
      }, 0);
    });
  },
  methods: {
    drawer() {
      const myChart1 = this.$echarts.init(document.getElementById("map1"));
      console.log(myChart1);
      myChart1.setOption(this.map1);
      window.addEventListener("resize", () => {
        myChart1.resize();
      });
    },
    drawer2() {
      const myChart2 = this.$echarts.init(document.getElementById("map2"));
      console.log(myChart2);
      myChart2.setOption(this.map2);
      window.addEventListener("resize", () => {
        myChart2.resize();
      });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.datav-content {
  width: 100vw;
  height: 100vh;
  background: #040c43;
  box-sizing: border-box;
  padding: 20px;
  min-height: 570px;
}
.grid-content {
  height: 100%;
}
.bg-purple {
  height: 48%;
}
.all-row {
  height: 100%;
}
.mb2 {
  margin-bottom: 2%;
}
.dp-flex {
  display: flex;
  flex-direction: column;
  /* align-items: center; */
  /* align-items: ; */
  justify-content: space-between;
}
.h40 {
  height: 40%;
}
.h56 {
  height: 56%;
}
.xm-style {
  display: flex;
  align-items: center;
  width: 100%;
  /* height: 100%; */
}
.dot {
  height: 10px;
  width: 10px;
  border-radius: 50%;
  background: #fff;
}
.C90A55 {
  color: #c90a55;
  background: #c90a55;
}
.CBFD {
  color: #45cbfd;
  background: #45cbfd;
}
.F7EFF {
  color: #6f7eff;
  background: #6f7eff;
}
.C545FE {
  color: #c545fe;
  background: #c545fe;
}
.mb3 {
  margin-bottom: 3px;
}
.dp-border {
  border-bottom: 1px solid rgba(255, 255, 255, 0.2);
  width: 100%;
  height: 22px;
  line-height: 22px;
}
::deep .dv-water-pond-level canvas {
  margin-left: -5px;
}
.pd15 {
  padding: 15px;
  box-sizing: border-box;
}
.pr20 {
  padding-right: 20px;
}
.map1 {
  width: 100%;
  height: calc(100% - 30px);
  padding: 0 30px;
  box-sizing: border-box;
  color: #fff;
  margin-top: -30px;
}
.map2 {
  width: 100%;
  height: calc(100% - 40px);
  padding: 0 30px;
  box-sizing: border-box;
  color: #fff;
}
::deep .dv-scroll-board .header {
  font-size: 12px;
}
</style>
