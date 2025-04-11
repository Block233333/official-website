<template>
  <div id="ServiceDetail">
    <div class="banner container-fuild text-center">相关服务</div>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-12 col-md-3" id="myScrollspy">
          <ul class="nav nav-tabs nav-stacked center-block" id="myNav">
            <p>特色服务</p>
            <li
              :class="item.id==id?'active':''"
              v-for="(item,index) in serviceNavList"
              :key="index"
            >
              <a :href="'#'+item.id">{{item.title}}</a>
            </li>
          </ul>
        </div>
        <div class="col-xs-12 col-sm-12 col-md-9 content  wow zoomIn">
          <div class="content-block" v-for="(item,index) in serviceContentList" :key="index">
            <h2 :id="item.id">
              {{item.title}}
              <small>/ {{item.eng_title}}</small>
            </h2>
            <div v-html="item.content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
export default {
  name: "ServiceDetail",
  data() {
    return {
      id: "section-1",
      serviceNavList: [
        {
          id: "section-1",
          title: "命运科学探究与咨询"
        },
        {
          id: "section-2",
          title: " 生命状态综合诊断"
        },
        {
          id: "section-3",
          title: "智能环境与运程优化"
        },
        {
          id: "section-4",
          title: "导师团队定制化指导"
        }
      ],
      serviceContentList: [
        {
          id: "section-1",
          title: "命运科学探究与咨询",
          eng_title: "Fate Science Research",
          content: `
            <h3>传统智慧与现代科学融合</h3>
            <p>基于四柱八字、紫微斗数等千年命理体系，结合天文学、生命科学等现代学科，构建「人地天命运观」模型。通过分析人体生理周期、自然节律与天体运行轨迹，精准解析个人命运轨迹，揭示事业、健康、情感的潜在规律，提供科学化命运解读报告。</p>
            <h3>全维度命运诊断</h3>
            <p>覆盖先天命格评估、流年运势预测、重大决策支持（如婚恋择期、职业转型）。运用梅花易数即时占卜技术，结合大数据模型验证，实现传统玄学与现代算法的双重校验，确保建议客观可信。</p>`
        },
        {
          id: "section-2",
          title: "生命状态综合诊断",
          eng_title: "Life Diagnosis",
          content: `
            <h3>双轨并行诊断体系</h3>
            <p>传统医学诊断：中医舌相/脉象辨识体质，藏医能量理论评估生命能量；现代医学检测：基因测序预测遗传风险，心理量表分析情绪状态。双轨数据交叉验证，生成个性化健康改善方案。</p>
            <h3>三维健康管理</h3>
            <p>生理层面定制中药调理与营养计划；心理层面提供正念训练与性格优化指导；精神层面通过禅修课程提升能量层级。定期追踪反馈，动态调整干预策略。</p>`
        },
        {
          id: "section-3",
          title: "智能环境与运程优化",
          eng_title: "Smart Optimization",
          content: `
            <h3>时空能量调节系统</h3>
            <p>智能提示引擎：依据出生八字与实时天文数据，推荐最佳决策时间（如签约、出行）；风水评估系统：通过3D建模分析住宅/办公室磁场，结合玄空飞星与环境科学，生成布局优化方案。</p>
            <h3>动态运程管理</h3>
            <p>接入可穿戴设备监测生理指标，同步气象与天体运行数据。当检测到「流年不利」征兆时，自动触发风水微调建议与能量场强化措施（如水晶阵布局、五行色彩搭配）。</p>`
        },
        {
          id: "section-4",
          title: "导师团队定制化指导",
          eng_title: "Expert Mentorship",
          content: `
            <h3>跨领域专家联盟</h3>
            <p>国学大师解读易经卦象，遗传学家分析基因潜能，心理医师疏导情绪障碍。多专家协同会诊，破解复杂人生困局（如家族业力传承、天赋与职业错配）。</p>
            <h3>全周期成长规划</h3>
            <p>儿童天赋开发：通过生辰八字与霍兰德测评定位发展方向；成人危机干预：结合大运周期设计转型路径（如创业时机选择）。提供年度运势沙盘推演与应急预案库，实现命运主动管理。</p>`
        }
      ]
    };
  },
  mounted() {
    this.id = this.$route.params.id;
    var top = document.getElementById(this.id).offsetTop;
    $(window).scrollTop(top + 300);
    $("#myNav").affix({
      offset: {
        top: 300
      }
    });
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
ul.nav-tabs {
  width: 200px;
  margin-top: 40px;
  border-radius: 4px;
  background: #fff;
  z-index: 99999;
  border: 1px solid #474747;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
}
ul.nav-tabs li {
  text-align: center;
  margin: 0;
  border-top: 1px solid #474747;
}
ul.nav-tabs p {
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  background: #474747;
  margin: 0;
  padding: 10px 0;
}
ul.nav-tabs li:first-child {
  border-top: none;
}
ul.nav-tabs li a {
  margin: 0;
  padding: 8px 16px;
  border-radius: 0;
}
ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #474747;
  border: 1px solid #474747;
}
ul.nav-tabs li:first-child a {
  border-radius: 4px 4px 0 0;
}
ul.nav-tabs li:last-child a {
  border-radius: 0 0 4px 4px;
}
ul.nav-tabs.affix {
  top: 30px;
}
.content-block {
  margin: 50px 0;
}
.content-block > h2 {
  padding: 20px 0;
  border-bottom: 1px solid #ccc;
}
</style>
