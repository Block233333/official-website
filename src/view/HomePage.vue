<template>
  <div id="HomePage">
    <!-- 轮播图 - 融合知命者大平台内容 -->
    <div id="hero-banner" class="container-fluid">
      <div class="swiper-container banner-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(item,index) in swiperList" :key="index">
            <img class="swiper-lazy" :data-src="item.img" alt="轮播图">
            <div class="swiper-lazy-preloader"></div>
            <div class="banner-content">
              <div class="banner-text-container">
                <h1 class="wow fadeInUp">{{item.title}}</h1>
                <p class="wow fadeInUp" data-wow-delay="0.3s">{{item.content}}</p>
                <div class="banner-buttons wow fadeInUp" data-wow-delay="0.6s">
                  <a href="#" class="btn btn-primary btn-lg">立即体验</a>
                  <a href="#" class="btn btn-outline-light btn-lg">了解更多</a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- 分页器 -->
        <div class="swiper-pagination"></div>
        <!-- 导航按钮 -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>
    </div>

    <!-- 平台导航 - 从SmartTown引入 -->
    <div class="platform-nav">
      <div class="container">
        <div class="nav-wrapper">
          <ul class="nav-tabs justify-content-center wow fadeInUp">
            <li class="active"><a href="#platform-intro">平台概述</a></li>
            <li><a href="#core-value">核心理念</a></li>
            <li><a href="#system-features">功能特色</a></li>
            <li><a href="#innovation">创新优势</a></li>
            <li><a href="#benefits">用户价值</a></li>
            <li><a href="#experts">专家团队</a></li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 平台介绍 - 从SmartTown引入 -->
    <div id="platform-intro" class="platform-intro section">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">双平台融合体系</h2>
          <p class="section-subtitle wow fadeInUp" data-wow-delay="0.2s">探索生命智慧，科学解读命运</p>
        </div>
        <div class="row platform-cards">
          <div class="col-md-6 wow fadeInLeft">
            <div class="platform-card">
              <div class="card-header">
                <div class="card-icon"><i class="fas fa-comments"></i></div>
                <h3>人生论坛</h3>
              </div>
              <ul class="platform-features">
                <li><i class="fas fa-lightbulb"></i> <strong>认识生命：</strong>探讨人活着的意义、价值，以及生死轮回等话题</li>
                <li><i class="fas fa-tools"></i> <strong>生存智慧：</strong>学习生存技能、生活知识和处世方法</li>
                <li><i class="fas fa-map"></i> <strong>人生规划：</strong>设定目标、找到方向、制定人生计划</li>
                <li><i class="fas fa-book"></i> <strong>传统智慧：</strong>中医、易经、风水等古老学问</li>
                <li><i class="fas fa-microscope"></i> <strong>现代知识：</strong>自然科学、西医、天文等工业时代学科</li>
              </ul>
            </div>
          </div>
          <div class="col-md-6 wow fadeInRight">
            <div class="platform-card">
              <div class="card-header">
                <div class="card-icon"><i class="fas fa-flask"></i></div>
                <h3>命运研究所</h3>
              </div>
              <ul class="platform-features">
                <li><i class="fas fa-search"></i> <strong>命运科学探究：</strong>用传统智慧+现代科技解读和改善命运</li>
                <li><i class="fas fa-stethoscope"></i> <strong>生命信息诊断：</strong>从基因到性格，从五脏六腑到运势潜能的全方位扫描</li>
                <li><i class="fas fa-chart-line"></i> <strong>运势轨迹预测：</strong>结合传统命理与现代科技预测人生关键节点</li>
                <li><i class="fas fa-sync-alt"></i> <strong>命运优化：</strong>通过身体调理、心理管理、时空调整改善命运</li>
                <li><i class="fas fa-users"></i> <strong>专家团队：</strong>传统命理师、中医师、心理学家、数据科学家联合服务</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 核心理念 - 从SmartTown引入 -->
    <div id="core-value" class="core-value section bg-light">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">核心理念</h2>
          <p class="section-subtitle wow fadeInUp" data-wow-delay="0.2s">传统与现代的完美结合，科学与人文的深度融合</p>
        </div>
        <div class="row mt-5">
          <div class="col-md-4 wow fadeInUp">
            <div class="value-card text-center">
              <div class="value-icon">
                <i class="fas fa-balance-scale"></i>
              </div>
              <h3>天人合一</h3>
              <p>人与自然和谐共生，顺应天道，尊重自然规律，实现身心与环境的平衡</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp" data-wow-delay="0.2s">
            <div class="value-card text-center">
              <div class="value-icon">
                <i class="fas fa-sync-alt"></i>
              </div>
              <h3>阴阳五行</h3>
              <p>万物相生相克，循环往复，通过平衡阴阳、调和五行，实现生命能量的最优配置</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp" data-wow-delay="0.4s">
            <div class="value-card text-center">
              <div class="value-icon">
                <i class="fas fa-dna"></i>
              </div>
              <h3>科学验证</h3>
              <p>运用现代科学方法验证传统理论，以数据分析和实证研究支持命理学的实践应用</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 系统功能 - 从SmartTown引入 -->
    <div id="system-features" class="system-features section">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">系统功能</h2>
          <p class="section-subtitle wow fadeInUp" data-wow-delay="0.2s">全方位的命理分析与生命优化工具</p>
        </div>
        <div class="row mt-5">
          <div class="col-lg-6 wow fadeInLeft">
            <div class="feature-image-placeholder">
              <i class="fas fa-chart-pie image-icon"></i>
              <p class="image-text">命理分析系统界面</p>
            </div>
          </div>
          <div class="col-lg-6 wow fadeInRight">
            <div class="feature-list">
              <div class="feature-item">
                <div class="feature-icon">
                  <i class="fas fa-user-check"></i>
                </div>
                <div class="feature-content">
                  <h3>个人命盘分析</h3>
                  <p>根据出生时间、地点等信息，生成详细的个人命盘，分析先天禀赋与潜能</p>
                </div>
              </div>
              <div class="feature-item">
                <div class="feature-icon">
                  <i class="fas fa-calendar-alt"></i>
                </div>
                <div class="feature-content">
                  <h3>运势预测</h3>
                  <p>分析大运、流年、流月等周期变化，预测人生关键点与转折点</p>
                </div>
              </div>
              <div class="feature-item">
                <div class="feature-icon">
                  <i class="fas fa-handshake"></i>
                </div>
                <div class="feature-content">
                  <h3>人际关系分析</h3>
                  <p>评估人际关系的相容性，提供婚姻、合作、亲子关系等方面的建议</p>
                </div>
              </div>
              <div class="feature-item">
                <div class="feature-icon">
                  <i class="fas fa-compass"></i>
                </div>
                <div class="feature-content">
                  <h3>方位与时间选择</h3>
                  <p>根据个人命盘，推荐有利的方位、时间，优化重要活动的安排</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 创新优势 - 从SmartTown引入 -->
    <div id="innovation" class="innovation section bg-light">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">创新优势</h2>
          <p class="section-subtitle wow fadeInUp" data-wow-delay="0.2s">传统智慧与现代科技的完美结合</p>
        </div>
        <div class="dual-approach mt-5">
          <div class="approach-card traditional wow fadeInLeft">
            <h3><i class="fas fa-history"></i> 传统方法</h3>
            <ul>
              <li>八字命理</li>
              <li>紫微斗数</li>
              <li>奇门遁甲</li>
              <li>风水堪舆</li>
              <li>中医理论</li>
            </ul>
          </div>
          <div class="approach-card modern wow fadeInRight">
            <h3><i class="fas fa-microchip"></i> 现代技术</h3>
            <ul>
              <li>大数据分析</li>
              <li>人工智能</li>
              <li>生物信息学</li>
              <li>心理学模型</li>
              <li>量子物理学</li>
            </ul>
          </div>
        </div>
        <div class="row mt-5">
          <div class="col-md-6 wow fadeInUp">
            <div class="innovation-item">
              <div class="innovation-icon">
                <i class="fas fa-database"></i>
              </div>
              <h3>海量数据支持</h3>
              <p>收集整理数百万历史案例，通过大数据分析验证传统理论的准确性和适用范围</p>
            </div>
          </div>
          <div class="col-md-6 wow fadeInUp" data-wow-delay="0.2s">
            <div class="innovation-item">
              <div class="innovation-icon">
                <i class="fas fa-robot"></i>
              </div>
              <h3>AI智能解读</h3>
              <p>运用人工智能技术，自动生成个性化的命理分析报告，提供精准的生活建议</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 用户受益 - 从SmartTown引入 -->
    <div id="benefits" class="benefits section">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">用户价值</h2>
          <p class="section-subtitle wow fadeInUp" data-wow-delay="0.2s">知命者平台为您带来的实际收益</p>
        </div>
        <div class="row mt-5">
          <div class="col-md-4 wow fadeInUp">
            <div class="benefit-card">
              <div class="benefit-icon">
                <i class="fas fa-lightbulb"></i>
              </div>
              <h3>自我认知</h3>
              <p>深入了解自己的性格特点、天赋潜能和发展方向，明确人生定位</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp" data-wow-delay="0.2s">
            <div class="benefit-card">
              <div class="benefit-icon">
                <i class="fas fa-route"></i>
              </div>
              <h3>生涯规划</h3>
              <p>根据个人命盘特点，选择适合的职业方向和发展路径，提高成功概率</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp" data-wow-delay="0.4s">
            <div class="benefit-card">
              <div class="benefit-icon">
                <i class="fas fa-heart"></i>
              </div>
              <h3>情感和谐</h3>
              <p>通过关系匹配分析，改善人际关系，提升婚恋质量和家庭幸福感</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp">
            <div class="benefit-card">
              <div class="benefit-icon">
                <i class="fas fa-shield-alt"></i>
              </div>
              <h3>风险防范</h3>
              <p>预知潜在风险期，提前做好应对准备，减少意外损失和健康隐患</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp" data-wow-delay="0.2s">
            <div class="benefit-card">
              <div class="benefit-icon">
                <i class="fas fa-hand-holding-usd"></i>
              </div>
              <h3>财富增长</h3>
              <p>把握财运高峰期，优化投资时机和方向，提高财富积累效率</p>
            </div>
          </div>
          <div class="col-md-4 wow fadeInUp" data-wow-delay="0.4s">
            <div class="benefit-card">
              <div class="benefit-icon">
                <i class="fas fa-spa"></i>
              </div>
              <h3>身心健康</h3>
              <p>了解体质特点和健康隐患，采取针对性的养生方案，提升生活质量</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 专家团队 - 从SmartTown引入 -->
    <div id="experts" class="experts section bg-light">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">专家团队</h2>
          <p class="section-subtitle wow fadeInUp" data-wow-delay="0.2s">跨学科精英，为您提供专业服务</p>
        </div>
        <div class="row mt-5">
          <div class="col-md-3 col-sm-6 wow fadeInUp">
            <div class="expert-card text-center">
              <div class="expert-avatar">
                <div class="avatar-placeholder">
                  <i class="fas fa-user"></i>
                </div>
              </div>
              <h3>张大师</h3>
              <p class="expert-title">首席命理顾问</p>
              <p class="expert-desc">30年命理实践经验，精通八字、紫微斗数</p>
            </div>
          </div>
          <div class="col-md-3 col-sm-6 wow fadeInUp" data-wow-delay="0.2s">
            <div class="expert-card text-center">
              <div class="expert-avatar">
                <div class="avatar-placeholder">
                  <i class="fas fa-user"></i>
                </div>
              </div>
              <h3>李博士</h3>
              <p class="expert-title">数据科学家</p>
              <p class="expert-desc">人工智能与大数据分析专家，负责系统算法开发</p>
            </div>
          </div>
          <div class="col-md-3 col-sm-6 wow fadeInUp" data-wow-delay="0.3s">
            <div class="expert-card text-center">
              <div class="expert-avatar">
                <div class="avatar-placeholder">
                  <i class="fas fa-user"></i>
                </div>
              </div>
              <h3>王教授</h3>
              <p class="expert-title">中医专家</p>
              <p class="expert-desc">中医学博士，擅长体质分析与养生调理</p>
            </div>
          </div>
          <div class="col-md-3 col-sm-6 wow fadeInUp" data-wow-delay="0.4s">
            <div class="expert-card text-center">
              <div class="expert-avatar">
                <div class="avatar-placeholder">
                  <i class="fas fa-user"></i>
                </div>
              </div>
              <h3>陈顾问</h3>
              <p class="expert-title">心理咨询师</p>
              <p class="expert-desc">心理学硕士，专注于个人成长与情感关系咨询</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 联系我们 - 从SmartTown引入 -->
    <div class="contact-section text-center">
      <div class="container">
        <h2 class="wow fadeInUp">开启您的生命探索之旅</h2>
        <p class="wow fadeInUp" data-wow-delay="0.2s">加入知命者平台，探索生命奥秘，掌握命运密码</p>
        <div class="contact-buttons wow fadeInUp" data-wow-delay="0.4s">
          <button class="btn btn-lg btn-primary">立即注册</button>
          <button class="btn btn-lg btn-outline-light">预约咨询</button>
        </div>
      </div>
    </div>

    <!-- 保留首页底部内容 -->
    <!-- 这里可以添加首页底部的内容 -->
  </div>
</template>

<script>
import { WOW } from 'wowjs';
import Swiper from 'swiper';
import 'swiper/dist/css/swiper.css';

export default {
  name: 'HomePage',
  data() {
    return {
      swiperList: [
        {
          img: require('@/assets/img/rollbanner1.jpeg'),
          title: '知命者大平台',
          content: '命运不是偶然，而是可以预测、可以调整、可以优化的科学'
        },
        {
          img: require('@/assets/img/rollbanner2.jpeg'),
          title: '传统智慧与现代科技的融合平台',
          content: '推动传统文化与现代科学的融合，为中华文化的传承与创新开辟全新发展道路'
        },
        {
          img: require('@/assets/img/rollbanner3.jpeg'),
          title: '探索生命智慧，科学解读命运',
          content: '知命而不惑，知命而不忧，知命而不惧，知命而不怨'
        }
      ]
    };
  },
  mounted() {
    // 初始化轮播图
    this.$nextTick(() => {
      new Swiper('.banner-swiper', {
        loop: true,
        autoplay: {
          delay: 5000,
          disableOnInteraction: false,
        },
        lazy: {
          loadPrevNext: true,
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
      });
    });

    // 初始化WOW.js动画
    new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: true
    }).init();
    
    // 添加平滑滚动效果
    document.querySelectorAll('.nav-tabs a').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        
        const targetId = this.getAttribute('href');
        const targetElement = document.querySelector(targetId);
        
        if (targetElement) {
          window.scrollTo({
            top: targetElement.offsetTop - 80,
            behavior: 'smooth'
          });
          
          // 更新活动标签
          document.querySelectorAll('.nav-tabs li').forEach(li => {
            li.classList.remove('active');
          });
          this.parentElement.classList.add('active');
        }
      });
    });
    
    // 监听滚动，更新导航状态
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const sections = ['platform-intro', 'core-value', 'system-features', 'innovation', 'benefits', 'experts'];
      const scrollPosition = window.scrollY + 100;
      
      for (const section of sections) {
        const element = document.getElementById(section);
        if (element) {
          const offsetTop = element.offsetTop;
          const offsetBottom = offsetTop + element.offsetHeight;
          
          if (scrollPosition >= offsetTop && scrollPosition < offsetBottom) {
            document.querySelectorAll('.nav-tabs li').forEach(li => {
              li.classList.remove('active');
            });
            
            const activeLink = document.querySelector(`.nav-tabs a[href="#${section}"]`);
            if (activeLink) {
              activeLink.parentElement.classList.add('active');
            }
            
            break;
          }
        }
      }
    }
  }
};
</script>

<style>
/* 轮播图样式 */
#hero-banner {
  padding: 0;
  position: relative;
}

.banner-swiper {
  width: 100%;
  height: 100vh;
  min-height: 600px;
}

.swiper-slide {
  position: relative;
  overflow: hidden;
}

.swiper-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.banner-content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  background: rgba(0, 0, 0, 0.5);
  color: white;
  z-index: 10; /* 添加适当的z-index值 */
}

.banner-text-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
  position: relative; /* 确保定位正确 */
  z-index: 11; /* 确保文字在最上层 */
}

.banner-content h1 {
  font-size: 48px;
  font-weight: 700;
  margin-bottom: 20px;
}

.banner-content p {
  font-size: 18px;
  margin-bottom: 30px;
  opacity: 0.9;
}

.banner-buttons {
  margin-top: 30px;
  position: relative;
  z-index: 12;
}

.banner-buttons .btn {
  margin: 0 10px;
  padding: 12px 30px;
  border-radius: 30px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-primary {
  background: #2575fc;
  color: white;
  border: none;
}

.btn-primary:hover {
  background: #1a68e5;
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.btn-outline-light {
  background: transparent;
  border: 2px solid white;
  color: white;
}

.btn-outline-light:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

/* 平台导航样式 */
.platform-nav {
  background: #fff;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.nav-wrapper {
  padding: 0;
}

.nav-tabs {
  display: flex;
  justify-content: center;
  border-bottom: none;
  margin: 0;
  padding: 0;
}

.nav-tabs li {
  margin: 0;
  list-style: none;
}

.nav-tabs li a {
  padding: 20px 25px;
  color: #555;
  font-size: 16px;
  font-weight: 500;
  border: none;
  border-bottom: 3px solid transparent;
  border-radius: 0;
  transition: all 0.3s ease;
  text-decoration: none;
  display: block;
}

.nav-tabs li a:hover {
  background: transparent;
  color: #2575fc;
}

.nav-tabs li.active a {
  color: #2575fc;
  background: transparent;
  border-bottom: 3px solid #2575fc;
}

/* 通用部分 */
.section {
  padding: 80px 0;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 15px;
}

.row {
  display: flex;
  flex-wrap: wrap;
  margin-right: -15px;
  margin-left: -15px;
}

.justify-content-center {
  justify-content: center;
}

.text-center {
  text-align: center;
}

.mt-5 {
  margin-top: 3rem;
}

.section-header {
  margin-bottom: 50px;
}

.section-header h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 15px;
  color: #333;
}

.section-subtitle {
  font-size: 18px;
  color: #666;
  max-width: 700px;
  margin: 0 auto;
}

.bg-light {
  background-color: #f8f9fa;
}

/* 平台介绍卡片样式 */
.platform-cards {
  margin-top: 50px;
}

.platform-card {
  background: white;
  border-radius: 12px;
  padding: 40px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  height: 100%;
  transition: all 0.3s ease;
  margin-bottom: 30px;
  border: 1px solid rgba(0,0,0,0.05);
}

.platform-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.card-header {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}

.card-icon {
  font-size: 30px;
  color: #2575fc;
  margin-right: 20px;
  width: 70px;
  height: 70px;
  background: rgba(37, 117, 252, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.platform-card:hover .card-icon {
  background: #2575fc;
  color: white;
  transform: scale(1.1);
}

.card-header h3 {
    font-size: 26px;
    margin: 0;
    font-weight: 600;
}

.platform-features {
    list-style: none;
    padding: 0;
}

.platform-features li {
    margin-bottom: 20px;
    font-size: 16px;
    display: flex;
    align-items: flex-start;
}

.platform-features i {
    color: #2575fc;
    margin-right: 15px;
    margin-top: 5px;
    font-size: 18px;
}

/* 核心理念部分 */
.bg-light {
    background-color: #f8f9fa;
}

.section-header {
    margin-bottom: 50px;
}

.section-header h2 {
    font-size: 36px;
    font-weight: 700;
    margin-bottom: 15px;
    color: #333;
}

.section-subtitle {
    font-size: 18px;
    color: #666;
    max-width: 700px;
    margin: 0 auto;
}

.value-card {
    padding: 30px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    transition: all 0.3s ease;
    height: 100%;
    margin-bottom: 30px;
}

.value-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.1);
}

.value-icon {
    font-size: 40px;
    color: #2575fc;
    margin-bottom: 20px;
}

.value-card h3 {
    font-size: 22px;
    margin-bottom: 15px;
    font-weight: 600;
}

.value-card p {
    color: #666;
    font-size: 16px;
    line-height: 1.6;
}

/* 系统功能部分 */
.feature-image-placeholder {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 300px;
    background: rgba(37, 117, 252, 0.05);
    border-radius: 8px;
    margin-bottom: 30px;
}

.feature-image-placeholder .image-icon {
    font-size: 60px;
    color: #2575fc;
    margin-bottom: 15px;
}

.feature-image-placeholder .image-text {
    font-size: 18px;
    color: #555;
}

.feature-list {
    padding: 20px 0;
}

.feature-item {
    display: flex;
    margin-bottom: 30px;
}

.feature-icon {
    flex: 0 0 60px;
    height: 60px;
    background: rgba(37, 117, 252, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 20px;
    font-size: 24px;
    color: #2575fc;
}

.feature-content {
    flex: 1;
}

.feature-content h3 {
    font-size: 20px;
    margin-bottom: 10px;
    font-weight: 600;
}

.feature-content p {
    color: #666;
    font-size: 16px;
    line-height: 1.6;
}

/* 创新优势部分 */
.dual-approach {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 30px;
}

.approach-card {
    flex: 1;
    min-width: 200px;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
}

.approach-card.traditional {
    background: rgba(106, 17, 203, 0.05);
}

.approach-card.modern {
    background: rgba(37, 117, 252, 0.05);
}

.approach-card h3 {
    font-size: 22px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
}

.approach-card h3 i {
    margin-right: 10px;
    color: #2575fc;
}

.approach-card ul {
    padding-left: 20px;
}

.approach-card ul li {
    margin-bottom: 10px;
    font-size: 16px;
}

.innovation-item {
    display: flex;
    background: white;
    border-radius: 10px;
    padding: 30px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    margin-bottom: 30px;
    transition: all 0.3s ease;
}

.innovation-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.1);
}

.innovation-icon {
    flex: 0 0 60px;
    height: 60px;
    background: rgba(37, 117, 252, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 20px;
    font-size: 24px;
    color: #2575fc;
}

.innovation-item h3 {
    font-size: 20px;
    margin-bottom: 10px;
    font-weight: 600;
}

.innovation-item p {
    color: #666;
    font-size: 16px;
    line-height: 1.6;
    margin: 0;
}

/* 用户受益部分 */
.benefit-card {
    background: white;
    border-radius: 10px;
    padding: 30px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    transition: all 0.3s ease;
    height: 100%;
    margin-bottom: 30px;
    text-align: center;
}

.benefit-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.1);
}

.benefit-icon {
    width: 80px;
    height: 80px;
    background: rgba(37, 117, 252, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-size: 30px;
    color: #2575fc;
}

.benefit-card h3 {
    font-size: 22px;
    margin-bottom: 15px;
    font-weight: 600;
}

.benefit-card p {
    color: #666;
    font-size: 16px;
    line-height: 1.6;
}

/* 专家团队部分 */
.expert-card {
    background: white;
    border-radius: 10px;
    padding: 30px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    transition: all 0.3s ease;
    height: 100%;
    margin-bottom: 30px;
}

.expert-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(0,0,0,0.1);
}

.expert-avatar {
    width: 120px;
    height: 120px;
    margin: 0 auto 20px;
    overflow: hidden;
    border-radius: 50%;
    background: #f5f5f5;
}

.avatar-placeholder {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(37, 117, 252, 0.1);
    font-size: 50px;
    color: #2575fc;
}

.expert-card h3 {
    font-size: 22px;
    margin-bottom: 5px;
    font-weight: 600;
}

.expert-title {
    color: #2575fc;
    font-size: 16px;
    margin-bottom: 15px;
}

.expert-desc {
    color: #666;
    font-size: 14px;
    line-height: 1.6;
}

/* 联系我们部分 */
.contact-section {
    background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
    color: white;
    padding: 80px 0;
    position: relative;
}

.contact-section h2 {
    font-size: 36px;
    font-weight: 700;
    margin-bottom: 15px;
}

.contact-section p {
    font-size: 18px;
    margin-bottom: 30px;
    opacity: 0.9;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
}

.contact-buttons {
    margin-top: 30px;
}

.contact-buttons .btn {
    margin: 0 10px;
    padding: 12px 30px;
    border-radius: 30px;
    font-weight: 600;
    transition: all 0.3s ease;
}

.btn-lg {
    padding: 15px 40px;
    font-size: 18px;
}

.btn-outline-light {
    background: transparent;
    border: 2px solid white;
    color: white;
}

.btn-outline-light:hover {
    background: rgba(255, 255, 255, 0.1);
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

/* 头部插图动画 */
.header-illustration {
    position: relative;
    width: 300px;
    height: 300px;
    margin: 0 auto;
}

.illustration-circle {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.1);
    animation: pulse 2s infinite;
}

.main-icon {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 80px;
    color: white;
}

.icon-orbit {
    position: absolute;
    font-size: 30px;
    color: rgba(255, 255, 255, 0.8);
}

.icon-1 {
    top: 20%;
    left: 20%;
    animation: orbit 15s linear infinite;
}

.icon-2 {
    top: 70%;
    left: 30%;
    animation: orbit 20s linear infinite reverse;
}

.icon-3 {
    top: 40%;
    left: 80%;
    animation: orbit 18s linear infinite;
}

@keyframes pulse {
    0% {
        box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.4);
    }
    70% {
        box-shadow: 0 0 0 20px rgba(255, 255, 255, 0);
    }
    100% {
        box-shadow: 0 0 0 0 rgba(255, 255, 255, 0);
    }
}

@keyframes orbit {
    0% {
        transform: rotate(0deg) translateX(100px) rotate(0deg);
    }
    100% {
        transform: rotate(360deg) translateX(100px) rotate(-360deg);
    }
}

/* 导航标签居中样式 */
.nav-tabs.justify-content-center {
    display: flex;
    justify-content: center;
    border-bottom: none;
}

/* 响应式调整 */
@media (max-width: 991px) {
    .nav-tabs li a {
        padding: 15px 15px;
        font-size: 14px;
    }
    
    .platform-card {
        padding: 30px;
    }
    
    .section-header h2 {
        font-size: 30px;
    }
    
    .banner-content h1 {
        font-size: 40px;
    }
}

@media (max-width: 767px) {
    .banner-swiper {
        height: 80vh;
        min-height: 500px;
    }
    
    .banner-content h1 {
        font-size: 32px;
    }
    
    .banner-content p {
        font-size: 16px;
    }
    
    .section {
        padding: 50px 0;
    }
    
    .nav-tabs {
        flex-wrap: nowrap;
        overflow-x: auto;
        justify-content: flex-start;
        padding: 0 10px;
    }
    
    .nav-tabs li a {
        padding: 15px 10px;
        white-space: nowrap;
    }
    
    .platform-card {
        padding: 25px;
    }
    
    .card-header {
        flex-direction: column;
        text-align: center;
    }
    
    .card-icon {
        margin-right: 0;
        margin-bottom: 15px;
    }
    
    .dual-approach {
        flex-direction: column;
    }
    
    .approach-card {
        margin-bottom: 15px;
    }
    
    .feature-item {
        flex-direction: column;
        text-align: center;
    }
    
    .feature-icon {
        margin: 0 auto 15px;
    }
    
    .innovation-item {
        flex-direction: column;
        text-align: center;
    }
    
    .innovation-icon {
        margin: 0 auto 15px;
    }
}

@media (max-width: 480px) {
    .banner-content h1 {
        font-size: 28px;
    }
    
    .banner-buttons .btn {
        display: block;
        width: 80%;
        margin: 0 auto 15px;
    }
    
    .section-header h2 {
        font-size: 26px;
    }
    
    .contact-buttons .btn {
        display: block;
        width: 80%;
        margin: 0 auto 15px;
    }
}

/* 动画效果 */
.wow {
    visibility: hidden;
}

.animated {
    animation-duration: 1s;
    animation-fill-mode: both;
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translate3d(0, 40px, 0);
    }
    to {
        opacity: 1;
        transform: translate3d(0, 0, 0);
    }
}

.fadeInUp {
    animation-name: fadeInUp;
}

@keyframes fadeInLeft {
    from {
        opacity: 0;
        transform: translate3d(-40px, 0, 0);
    }
    to {
        opacity: 1;
        transform: translate3d(0, 0, 0);
    }
}

.fadeInLeft {
    animation-name: fadeInLeft;
}

@keyframes fadeInRight {
    from {
        opacity: 0;
        transform: translate3d(40px, 0, 0);
    }
    to {
        opacity: 1;
        transform: translate3d(0, 0, 0);
    }
}

.fadeInRight {
    animation-name: fadeInRight;
}

@keyframes zoomIn {
    from {
        opacity: 0;
        transform: scale3d(0.3, 0.3, 0.3);
    }
    50% {
        opacity: 1;
    }
}

.zoomIn {
    animation-name: zoomIn;
}

/* 列布局样式 */
.col-md-3, .col-md-4, .col-md-6, .col-md-10, .col-lg-6, .col-sm-6 {
    position: relative;
    width: 100%;
    padding-right: 15px;
    padding-left: 15px;
}

@media (min-width: 576px) {
    .col-sm-6 {
        flex: 0 0 50%;
        max-width: 50%;
    }
}

@media (min-width: 768px) {
    .col-md-3 {
        flex: 0 0 25%;
        max-width: 25%;
    }
    .col-md-4 {
        flex: 0 0 33.333333%;
        max-width: 33.333333%;
    }
    .col-md-6 {
        flex: 0 0 50%;
        max-width: 50%;
    }
    .col-md-10 {
        flex: 0 0 83.333333%;
        max-width: 83.333333%;
    }
}

@media (min-width: 992px) {
    .col-lg-6 {
        flex: 0 0 50%;
        max-width: 50%;
    }
}

/* 底部样式 - 保留首页原有底部 */
.footer {
    background: #333;
    color: #fff;
    padding: 40px 0;
}

.footer-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.footer-section {
    flex: 1;
    min-width: 200px;
    margin-bottom: 20px;
    padding: 0 15px;
}

.footer-section h3 {
    font-size: 18px;
    margin-bottom: 20px;
    color: #fff;
}

.footer-section ul {
    list-style: none;
    padding: 0;
}

.footer-section ul li {
    margin-bottom: 10px;
}

.footer-section ul li a {
    color: #ccc;
    text-decoration: none;
    transition: color 0.3s ease;
}

.footer-section ul li a:hover {
    color: #fff;
}

.footer-bottom {
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    padding-top: 20px;
    margin-top: 20px;
    text-align: center;
    color: #ccc;
}
</style>

