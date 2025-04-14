<template>
  <div id="ServiceDetail">
    <!-- 页面顶部横幅 -->
    <div class="banner container-fluid">
      <div class="banner-overlay"></div>
      <div class="banner-content text-center">
        <h1 class="wow fadeInUp">服务详情</h1>
        <div class="banner-divider wow fadeInUp" data-wow-delay="0.2s"></div>
        <p class="wow fadeInUp" data-wow-delay="0.4s">探索命运科学的奥秘，开启人生新篇章</p>
      </div>
    </div>
    
    <div class="container service-detail-section">
      <div class="row">
        <!-- 侧边导航 -->
        <div class="col-xs-12 col-sm-12 col-md-3" id="myScrollspy">
          <div class="sidebar-nav wow fadeInLeft">
            <div class="sidebar-header">
              <h3>特色服务</h3>
            </div>
            <ul class="nav nav-tabs nav-stacked center-block" id="myNav">
              <li
                :class="item.id==id?'active':''"
                v-for="(item,index) in serviceNavList"
                :key="index"
              >
                <a :href="'#'+item.id">
                  <span class="nav-icon"><i class="fa" :class="getIconClass(index)"></i></span>
                  <span class="nav-text">{{item.title}}</span>
                </a>
              </li>
            </ul>
            
            <div class="sidebar-cta">
              <h4>需要更多帮助？</h4>
              <p>我们的专家团队随时为您提供个性化咨询</p>
              <button class="btn btn-primary btn-block" @click="contactUs">联系我们</button>
            </div>
          </div>
        </div>
        
        <!-- 内容区域 -->
        <div class="col-xs-12 col-sm-12 col-md-9 content">
          <div class="content-block wow fadeInUp" v-for="(item,index) in serviceContentList" :key="index" :data-wow-delay="0.2 * index + 's'">
            <div class="service-header" :id="item.id">
              <div class="service-icon">
                <i class="fa" :class="getIconClass(index)"></i>
              </div>
              <div class="service-title">
                <h2>
                  {{item.title}}
                  <small>/ {{item.eng_title}}</small>
                </h2>
              </div>
            </div>
            <div class="service-content" v-html="item.content"></div>
            
            <div class="service-features">
              <div class="feature-item" v-for="(feature, fIndex) in getFeatures(index)" :key="fIndex">
                <div class="feature-icon">
                  <i class="fa fa-check-circle"></i>
                </div>
                <div class="feature-text">
                  <p>{{feature}}</p>
                </div>
              </div>
            </div>
            
            <div class="service-action">
              <button class="btn btn-primary" @click="contactUs">咨询此服务</button>
              <button class="btn btn-outline" @click="goBack">返回服务列表</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- 相关服务推荐 -->
    <div class="related-services container-fluid">
      <div class="container">
        <div class="section-header text-center wow fadeInUp">
          <h2 class="section-title">您可能还需要</h2>
          <div class="section-divider center-divider"></div>
          <p class="section-description">探索我们的其他服务，获取全方位的命运优化方案</p>
        </div>
        
        <div class="row">
          <div class="col-md-4 col-sm-6 wow fadeInUp" v-for="(item, index) in getRelatedServices()" :key="index" :data-wow-delay="0.2 * index + 's'">
            <div class="related-service-card" @click="ServiceClick(item.id)">
              <div class="card-image">
                <img :src="item.img" alt="相关服务">
              </div>
              <div class="card-content">
                <h3>{{item.title}}</h3>
                <p>{{item.eng_title}}</p>
                <a href="javascript:void(0)" class="read-more">了解更多 <i class="fa fa-arrow-right"></i></a>
              </div>
            </div>
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
          title: "生命状态综合诊断"
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
          img: require('@/assets/img/service1.jpeg'),
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
          img: require('@/assets/img/service2.jpeg'),
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
          img: require('@/assets/img/service3.jpeg'),
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
          img: require('@/assets/img/service4.jpeg'),
          content: `
            <h3>跨领域专家联盟</h3>
            <p>国学大师解读易经卦象，遗传学家分析基因潜能，心理医师疏导情绪障碍。多专家协同会诊，破解复杂人生困局（如家族业力传承、天赋与职业错配）。</p>
            <h3>全周期成长规划</h3>
            <p>儿童天赋开发：通过生辰八字与霍兰德测评定位发展方向；成人危机干预：结合大运周期设计转型路径（如创业时机选择）。提供年度运势沙盘推演与应急预案库，实现命运主动管理。</p>`
        }
      ],
      serviceFeatures: {
        "section-1": [
          "个人命运轨迹精准解析",
          "重大人生决策科学支持",
          "传统命理与现代科技结合",
          "客观可信的双重验证系统"
        ],
        "section-2": [
          "中西医结合的全面诊断",
          "个性化健康改善方案",
          "身心灵三维一体调理",
          "动态追踪反馈系统"
        ],
        "section-3": [
          "智能决策时间推荐",
          "专业风水环境评估",
          "实时生理指标监测",
          "自动化能量场调节"
        ],
        "section-4": [
          "多领域专家团队支持",
          "复杂人生困局破解",
          "全生命周期规划指导",
          "定制化成长方案设计"
        ]
      }
    };
  },
  methods: {
    getIconClass(index) {
      const icons = ["fa-compass", "fa-heartbeat", "fa-cogs", "fa-users"];
      return icons[index] || "fa-star";
    },
    getFeatures(index) {
      const id = this.serviceContentList[index].id;
      return this.serviceFeatures[id] || [];
    },
    getRelatedServices() {
      // 获取除当前服务外的其他服务
      return this.serviceContentList
        .filter(item => item.id !== this.id)
        .slice(0, 3);
    },
    ServiceClick(id) {
      this.$router.push({
        name: 'servicedetail',
        params: {
          id: id
        }
      });
    },
    contactUs() {
      // 设置导航索引为"联系我们"
      sessionStorage.setItem('navIndex', 6);
      this.$router.push({
        name: 'contactus',
        query: { scrollTop: 0 } // 添加查询参数，确保页面从顶部开始显示
      });
    },
    
    goBack() {
      // 设置导航索引为"公司服务"
      sessionStorage.setItem('navIndex', 2);
      this.$router.push({
        name: 'service'
      });
    }
  },
  mounted() {
    this.id = this.$route.params.id || "section-1";
    
    // 初始化滚动位置
    this.$nextTick(() => {
      const element = document.getElementById(this.id);
      if (element) {
        const top = element.offsetTop;
        window.scrollTo({
          top: top - 100,
          behavior: 'smooth'
        });
      }
    });
    
    // 初始化侧边栏固定效果
    $(document).ready(function() {
      $("#myNav").affix({
        offset: {
          top: 300
        }
      });
    });
    
    // 初始化动画
    var wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 100,
      mobile: true,
      live: true
    });
    wow.init();
  }
};
</script>

<style scoped>
/* 全局样式 */
#ServiceDetail {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  color: #333;
  line-height: 1.6;
}

/* 横幅样式 */
.banner {
  position: relative;
  height: 350px;
  color: #fff;
  font-size: 30px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.banner-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

.banner-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
  padding: 0 20px;
}

.banner-content h1 {
  font-size: 48px;
  font-weight: 700;
  margin-bottom: 20px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

.banner-content p {
  font-size: 20px;
  margin-bottom: 30px;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
}

.banner-divider {
  width: 80px;
  height: 3px;
  background-color: #fff;
  margin: 0 auto 20px;
}

/* 服务详情区域样式 */
.service-detail-section {
  padding: 80px 0;
}

/* 侧边导航样式 */
.sidebar-nav {
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  overflow: hidden;
  margin-bottom: 30px;
}

.sidebar-header {
  background: #2c3e50;
  padding: 20px;
  text-align: center;
}

.sidebar-header h3 {
  color: #fff;
  font-size: 20px;
  font-weight: 600;
  margin: 0;
}

ul.nav-tabs {
  width: 100%;
  margin: 0;
  border: none;
  box-shadow: none;
}

ul.nav-tabs li {
  text-align: left;
  margin: 0;
  border-top: 1px solid #eee;
}

ul.nav-tabs li a {
  margin: 0;
  padding: 15px 20px;
  border-radius: 0;
  color: #555;
  font-size: 15px;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
}

ul.nav-tabs li a:hover {
  background-color: rgba(52, 152, 219, 0.05);
  color: #3498db;
}

ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #3498db;
  border: none;
}

.nav-icon {
  width: 30px;
  height: 30px;
  background-color: rgba(52, 152, 219, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 10px;
}

.nav-icon i {
  font-size: 14px;
  color: #3498db;
}

li.active .nav-icon {
  background-color: rgba(255, 255, 255, 0.2);
}

li.active .nav-icon i {
  color: #fff;
}

.sidebar-cta {
  padding: 20px;
  background-color: #f8f9fa;
  border-top: 1px solid #eee;
}

.sidebar-cta h4 {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 10px;
  color: #2c3e50;
}

.sidebar-cta p {
  font-size: 14px;
  color: #666;
  margin-bottom: 15px;
}

.sidebar-cta .btn {
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: 500;
  background-color: #3498db;
  border-color: #3498db;
  color: #fff;
  transition: all 0.3s ease;
}

.sidebar-cta .btn:hover {
  background-color: #2980b9;
  border-color: #2980b9;
}

/* 内容区域样式 */
.content {
  padding: 0 20px;
}

.content-block {
  margin-bottom: 80px;
  padding-bottom: 40px;
  border-bottom: 1px solid #eee;
}

.content-block:last-child {
  border-bottom: none;
  margin-bottom: 0;
}

.service-header {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}

.service-icon {
  width: 60px;
  height: 60px;
  background-color: rgba(52, 152, 219, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 20px;
  flex-shrink: 0;
}

.service-icon i {
  font-size: 28px;
  color: #3498db;
}

.service-title h2 {
  font-size: 28px;
  font-weight: 700;
  margin: 0;
  color: #2c3e50;
}

.service-title h2 small {
  font-size: 16px;
  color: #95a5a6;
  font-weight: 400;
}

.service-content {
  margin-bottom: 30px;
}

.service-content h3 {
  font-size: 20px;
  font-weight: 600;
  margin: 25px 0 15px;
  color: #2c3e50;
}

.service-content p {
  font-size: 16px;
  line-height: 1.8;
  color: #555;
  margin-bottom: 20px;
  text-align: justify;
}

/* 服务特点样式 */
.service-features {
  background-color: #f8f9fa;
  border-radius: 10px;
  padding: 25px;
  margin-bottom: 30px;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  margin-bottom: 15px;
}

.feature-item:last-child {
  margin-bottom: 0;
}

.feature-icon {
  margin-right: 15px;
  flex-shrink: 0;
}

.feature-icon i {
  font-size: 18px;
  color: #3498db;
}

.feature-text p {
  font-size: 15px;
  color: #555;
  margin: 0;
}

/* 服务操作按钮 */
.service-action {
  display: flex;
  gap: 15px;
}

.service-action .btn {
  padding: 12px 25px;
  border-radius: 5px;
  font-weight: 500;
  transition: all 0.3s ease;
}

.btn-primary {
  background-color: #3498db;
  border-color: #3498db;
  color: #fff;
}

.btn-primary:hover {
  background-color: #2980b9;
  border-color: #2980b9;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.btn-outline {
  background-color: transparent;
  border: 1px solid #3498db;
  color: #3498db;
}

.btn-outline:hover {
  background-color: rgba(52, 152, 219, 0.05);
  transform: translateY(-2px);
}

/* 相关服务推荐样式 */
.related-services {
  background-color: #f8f9fa;
  padding: 80px 0;
  margin-top: 50px;
}

.related-service-card {
  background-color: #fff;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  margin-bottom: 30px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.related-service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.card-image {
  height: 200px;
  overflow: hidden;
}

.card-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: all 0.5s ease;
}

.related-service-card:hover .card-image img {
  transform: scale(1.1);
}

.card-content {
  padding: 25px;
}

.card-content h3 {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 10px;
  color: #2c3e50;
}

.card-content p {
  font-size: 14px;
  color: #95a5a6;
  margin-bottom: 15px;
}

.read-more {
  font-size: 14px;
  font-weight: 500;
  color: #3498db;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
}

.read-more i {
  margin-left: 5px;
  transition: all 0.3s ease;
}

.related-service-card:hover .read-more i {
  transform: translateX(5px);
}

/* 响应式调整 */
@media (max-width: 991px) {
  .banner {
    height: 300px;
  }
  
  .banner-content h1 {
    font-size: 36px;
  }
  
  .banner-content p {
    font-size: 18px;
  }
  
  .service-detail-section {
    padding: 60px 0;
  }
  
  .sidebar-nav {
    margin-bottom: 40px;
  }
  
  .service-title h2 {
    font-size: 24px;
  }
}

@media (max-width: 767px) {
  .banner {
    height: 250px;
  }
  
  .banner-content h1 {
    font-size: 30px;
  }
  
  .banner-content p {
    font-size: 16px;
  }
  
  .service-detail-section {
    padding: 40px 0;
  }
  
  .content {
    padding: 0;
  }
  
  .service-header {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .service-icon {
    margin-bottom: 15px;
  }
  
  .service-action {
    flex-direction: column;
  }
  
  .service-action .btn {
    width: 100%;
    margin-bottom: 10px;
  }
}

@media (max-width: 480px) {
  .banner {
    height: 200px;
  }
  
  .banner-content h1 {
    font-size: 24px;
  }
  
  .banner-content p {
    font-size: 14px;
  }
  
  .service-title h2 {
    font-size: 20px;
  }
  
  .service-title h2 small {
    display: block;
    margin-top: 5px;
  }
  
  .service-content h3 {
    font-size: 18px;
  }
  
  .service-content p {
    font-size: 15px;
  }
}

/* 动画效果 */
.wow {
  visibility: hidden;
}
</style>
