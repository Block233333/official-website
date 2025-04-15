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
                <!-- 移除 wow 类，改用 v-show 控制显示 -->
                <h1 v-show="true">{{item.title}}</h1>
                <p v-show="true">{{item.content}}</p>
                <div class="banner-buttons" v-show="true">
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

    <!-- 添加平台使命部分 -->
<div class="mission-section">
  <div class="container">
    <div class="mission-content">
      <div class="mission-header text-center wow fadeInUp">
        <h2>知命者平台使命</h2>
        <div class="divider"></div>
      </div>
      <div class="mission-body">
        <div class="mission-quote wow fadeIn" data-wow-delay="0.2s">
          <span class="quote-mark">"</span>
          <p>揭示命运真相，赋能人生优化</p>
          <span class="quote-mark closing">"</span>
        </div>
        <div class="mission-text wow fadeIn" data-wow-delay="0.4s">
          <p>《知命者》以"利人利己"的传统精神为根基，恪守"合法合理"的行动准则，致力于构建系统化的命运科学体系，帮助大众认知命运本质、树立科学命运观，并传播切实可行的改运方法。</p>
          <p>平台通过整合传统智慧与现代知识，助力用户突破命运障碍、化解生存危机，同时为专业人士提供实践舞台，使其在服务他人中实现个人价值，最终推动所有人从命运科学中受益，迈向更顺畅、更美好的人生道路。</p>
        </div>
        <div class="mission-values wow fadeInUp" data-wow-delay="0.6s">
          <div class="value-item">
            <div class="value-icon">
              <i class="fas fa-handshake"></i>
            </div>
            <h4>利人利己</h4>
          </div>
          <div class="value-item">
            <div class="value-icon">
              <i class="fas fa-balance-scale"></i>
            </div>
            <h4>合法合理</h4>
          </div>
          <div class="value-item">
            <div class="value-icon">
              <i class="fas fa-lightbulb"></i>
            </div>
            <h4>科学命运观</h4>
          </div>
          <div class="value-item">
            <div class="value-icon">
              <i class="fas fa-hands-helping"></i>
            </div>
            <h4>赋能成长</h4>
          </div>
        </div>
      </div>
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
                <h3 class="card-title">人生论坛</h3>
              </div>
              <ul class="platform-features">
                <li><i class="fas fa-lightbulb"></i> <strong>认识生命：</strong>探讨人生的意义、价值，以及生死轮回等话题</li>
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
                <h3 class="card-title">命运研究所</h3>
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

    <!-- 系统功能 -->
    <div id="system-features" class="system-features section">
      <div class="container">
        <div class="section-header text-center">
          <h2 class="wow fadeInUp">平台功能</h2>
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
              <p>整理搭建命理知识库，通过大数据分析验证传统理论的准确性和适用范围</p>
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
          loadOnTransitionStart: true, // 添加这一行
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
        on: {  // 添加事件监听
          slideChange: function () {
            // 确保切换时内容可见
            const activeSlide = this.slides[this.activeIndex];
            if (activeSlide) {
              const content = activeSlide.querySelector('.banner-content');
              if (content) {
                content.style.opacity = '1';
              }
            }
          }
        }
      });
    });

    // 初始化WOW.js动画
    this.wowInstance = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: false // 修改为false，因为MutationObserver不被支持
    });
    this.wowInstance.init();

    // 手动同步WOW动画
    setTimeout(() => {
      if (this.wowInstance && typeof this.wowInstance.sync === 'function') {
        this.wowInstance.sync();
      }
    }, 500);
    
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
  updated() {
    // 在组件更新后再次同步WOW动画
    this.$nextTick(() => {
      if (this.wowInstance && typeof this.wowInstance.sync === 'function') {
        this.wowInstance.sync();
      }
    });
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const sections = ['mission-section', 'core-value', 'system-features', 'innovation', 'benefits', 'experts'];
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
<style scoped>
/* 修改配色方案 - 融合传统与现代 */
:root {
  --primary-color: #8e44ad; /* 紫色：代表神秘、智慧 */
  --secondary-color: #3498db; /* 蓝色：代表科技、现代 */
  --accent-color: #f39c12; /* 金色：代表传统、尊贵 */
  --dark-color: #2c3e50; /* 深蓝灰：稳重 */
  --light-color: #f8f9fa; /* 浅灰：现代感 */
  --gradient-primary: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  --gradient-secondary: linear-gradient(135deg, #f39c12 0%, #e74c3c 100%);
}

/* 轮播图样式优化 */
#hero-banner {
  padding: 0;
  position: relative;
}

.banner-swiper {
  width: 100%;
  height: 70vh;
  min-height: 500px;
}

.swiper-slide {
  position: relative;
  overflow: hidden;
}

.swiper-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: saturate(1.2); /* 增强图片饱和度 */
}

.banner-content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  background: rgba(0, 0, 0, 0.6); /* 加深遮罩 */
  color: white;
  z-index: 10;
}

.banner-text-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
  position: relative;
  z-index: 11;
}

.banner-content h1 {
  font-size: 48px;
  font-weight: 700;
  margin-bottom: 20px;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5); /* 添加文字阴影 */
  letter-spacing: 2px; /* 增加字间距 */
}

.banner-content p {
  font-size: 18px;
  margin-bottom: 30px;
  opacity: 0.9;
  text-shadow: 0 2px 5px rgba(0, 0, 0, 0.5); /* 添加文字阴影 */
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
  background: var(--primary-color);
  color: white;
  border: none;
  box-shadow: 0 4px 15px rgba(142, 68, 173, 0.3); /* 添加阴影 */
}

.btn-primary:hover {
  background: #7d3c98; /* 深紫色 */
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(142, 68, 173, 0.4);
}

.btn-outline-light {
  background: transparent;
  border: 2px solid white;
  color: white;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.btn-outline-light:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

/* 平台导航样式优化 */
.platform-nav {
  background: white;
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
  color: var(--dark-color);
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
  color: var(--primary-color);
}

.nav-tabs li.active a {
  color: var(--primary-color);
  background: transparent;
  border-bottom: 3px solid var(--primary-color);
}

/* 通用部分样式优化 */
.section {
  padding: 100px 0; /* 增加内边距 */
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 15px;
}

.section-header {
  margin-bottom: 60px; /* 增加间距 */
}

.section-header h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 15px;
  color: var(--dark-color);
  position: relative;
  display: inline-block;
}

.section-header h2:after {
  content: "";
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 3px;
  background: var(--gradient-primary);
  border-radius: 3px;
}

.section-subtitle {
  font-size: 18px;
  color: #666;
  max-width: 700px;
  margin: 20px auto 0;
}

.bg-light {
  background-color: #f8f9fa;
  background-image: url('data:image/svg+xml;utf8,<svg width="20" height="20" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><rect width="20" height="20" fill="none"/><circle cx="3" cy="3" r="1" fill="%23f0f0f0"/></svg>');
  background-size: 20px 20px;
}

/* 平台介绍卡片样式优化 */
.platform-cards {
  margin-top: 50px;
}

.platform-card {
  background: white;
  border-radius: 15px;
  padding: 40px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  height: 100%;
  transition: all 0.3s ease;
  margin-bottom: 30px;
  border: 1px solid rgba(0,0,0,0.05);
  position: relative;
  overflow: hidden;
}

.platform-card:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 5px;
  background: var(--gradient-primary);
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
  color: white;
  margin-right: 20px;
  width: 70px;
  height: 70px;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  box-shadow: 0 5px 15px rgba(142, 68, 173, 0.3);
}

.platform-card:hover .card-icon {
  transform: scale(1.1) rotate(5deg);
}

.card-header h3 {
  font-size: 26px;
  margin: 0;
  font-weight: 600;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  background-clip: text; /* 添加标准属性以提高兼容性 */
  -webkit-text-fill-color: transparent;
  color: transparent; /* 为不支持 -webkit-text-fill-color 的浏览器添加备选方案 */
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
  transition: all 0.3s ease;
}

.platform-features li:hover {
  transform: translateX(5px);
}

.platform-features i {
  color: var(--primary-color);
  margin-right: 15px;
  margin-top: 5px;
  font-size: 18px;
}

/* 核心理念部分样式优化 */
.value-card {
  padding: 40px 30px;
  background: white;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  height: 100%;
  margin-bottom: 30px;
  position: relative;
  overflow: hidden;
  z-index: 1;
}

.value-card:before {
  content: "";
  position: absolute;
  bottom: 0;
  right: 0;
  width: 100px;
  height: 100px;
  background: var(--gradient-primary);
  opacity: 0.1;
  border-radius: 50%;
  transform: translate(30%, 30%);
  z-index: -1;
  transition: all 0.3s ease;
}

.value-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.value-card:hover:before {
  transform: scale(3) translate(20%, 20%);
}

.value-icon {
  font-size: 40px;
  width: 90px;
  height: 90px;
  line-height: 90px;
  margin: 0 auto 25px;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  box-shadow: 0 10px 20px rgba(142, 68, 173, 0.3);
  transition: all 0.3s ease;
}

.value-card:hover .value-icon {
  transform: rotateY(180deg);
}

.value-card h3 {
  font-size: 22px;
  margin-bottom: 15px;
  font-weight: 600;
  color: var(--primary-color);
}

.value-card p {
  color: #666;
  font-size: 16px;
  line-height: 1.6;
}

/* 系统功能部分样式优化 */
.feature-image-placeholder {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 350px;
  background: rgba(142, 68, 173, 0.05);
  border-radius: 15px;
  margin-bottom: 30px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
}

.feature-image-placeholder:before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(
    to bottom right,
    rgba(142, 68, 173, 0.1) 0%,
    rgba(52, 152, 219, 0.1) 50%,
    rgba(243, 156, 18, 0.1) 100%
  );
  transform: rotate(30deg);
  animation: gradientMove 10s linear infinite;
}

@keyframes gradientMove {
  0% {
    transform: rotate(30deg) translateY(0);
  }
  50% {
    transform: rotate(30deg) translateY(5%);
  }
  100% {
    transform: rotate(30deg) translateY(0);
  }
}

.feature-image-placeholder .image-icon {
  font-size: 80px;
  color: var(--primary-color);
  margin-bottom: 15px;
  position: relative;
  z-index: 2;
}

.feature-image-placeholder .image-text {
  font-size: 18px;
  color: var(--dark-color);
  position: relative;
  z-index: 2;
}

.feature-list {
  padding: 20px 0;
}

.feature-item {
  display: flex;
  margin-bottom: 30px;
  transition: all 0.3s ease;
}

.feature-item:hover {
  transform: translateX(5px);
}

.feature-icon {
  flex: 0 0 60px;
  height: 60px;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 20px;
  font-size: 24px;
  color: white;
  box-shadow: 0 5px 15px rgba(142, 68, 173, 0.3);
}

.feature-content {
  flex: 1;
}

.feature-content h3 {
  font-size: 20px;
  margin-bottom: 10px;
  font-weight: 600;
  color: var(--primary-color);
}

.feature-content p {
  color: #666;
  font-size: 16px;
  line-height: 1.6;
}

/* 创新优势部分样式优化 */
.dual-approach {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  margin-bottom: 40px;
}

.approach-card {
  flex: 1;
  min-width: 200px;
  padding: 40px 30px;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
}

.approach-card.traditional {
  background: white;
  border-left: 5px solid var(--accent-color);
}

.approach-card.traditional:before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 150px;
  height: 150px;
  background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><circle cx="50" cy="50" r="40" stroke="%23f39c12" stroke-width="2" fill="none" stroke-dasharray="5,5"/></svg>');
  background-size: contain;
  opacity: 0.2;
}

.approach-card.modern {
  background: white;
  border-left: 5px solid var(--secondary-color);
}

.approach-card.modern:before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 150px;
  height: 150px;
  background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><rect x="20" y="20" width="60" height="60" stroke="%233498db" stroke-width="2" fill="none" stroke-dasharray="5,5"/></svg>');
  background-size: contain;
  opacity: 0.2;
}

.approach-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.approach-card h3 {
  font-size: 22px;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  position: relative;
}

.approach-card.traditional h3 {
  color: var(--accent-color);
}

.approach-card.modern h3 {
  color: var(--secondary-color);
}

.approach-card h3 i {
  margin-right: 10px;
}

.approach-card ul {
  padding-left: 20px;
  position: relative;
  z-index: 2;
}

.approach-card ul li {
  margin-bottom: 15px;
  font-size: 16px;
  position: relative;
}

.approach-card.traditional ul li:before {
  content: "☯";
  position: absolute;
  left: -20px;
  color: var(--accent-color);
}

.approach-card.modern ul li:before {
  content: "⚛";
  position: absolute;
  left: -20px;
  color: var(--secondary-color);
}

.innovation-item {
  display: flex;
  background: white;
  border-radius: 15px;
  padding: 30px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  margin-bottom: 30px;
  transition: all 0.3s ease;
  border-left: 5px solid var(--primary-color);
}

.innovation-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.innovation-icon {
  flex: 0 0 60px;
  height: 60px;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 20px;
  font-size: 24px;
  color: white;
  box-shadow: 0 5px 15px rgba(142, 68, 173, 0.3);
}

.innovation-item h3 {
  font-size: 20px;
  margin-bottom: 10px;
  font-weight: 600;
  color: var(--primary-color);
}

.innovation-item p {
  color: #666;
  font-size: 16px;
  line-height: 1.6;
  margin: 0;
}

/* 用户受益部分样式优化 */
.benefit-card {
  background: white;
  border-radius: 15px;
  padding: 40px 30px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  height: 100%;
  margin-bottom: 30px;
  text-align: center;
  position: relative;
  overflow: hidden;
  z-index: 1;
}

.benefit-card:after {
  content: "";
  position: absolute;
  bottom: -50%;
  right: -50%;
  width: 100%;
  height: 100%;
  background: var(--gradient-primary);
  opacity: 0.05;
  border-radius: 50%;
  z-index: -1;
  transition: all 0.5s ease;
}

.benefit-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.benefit-card:hover:after {
  transform: scale(2);
}

.benefit-icon {
  width: 90px;
  height: 90px;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 25px;
  font-size: 35px;
  color: white;
  box-shadow: 0 10px 20px rgba(142, 68, 173, 0.3);
  transition: all 0.3s ease;
}

.benefit-card:hover .benefit-icon {
  transform: scale(1.1);
}

.benefit-card h3 {
  font-size: 22px;
  margin-bottom: 15px;
  font-weight: 600;
  color: var(--primary-color);
}

.benefit-card p {
  color: #666;
  font-size: 16px;
  line-height: 1.6;
}

/* 专家团队部分样式优化 */
.expert-card {
  background: white;
  border-radius: 15px;
  padding: 40px 30px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  height: 100%;
  margin-bottom: 30px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.expert-card:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 120px;
  background: var(--gradient-primary);
  opacity: 0.1;
  z-index: 0;
}

.expert-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.expert-avatar {
  width: 120px;
  height: 120px;
  margin: 0 auto 20px;
  overflow: hidden;
  border-radius: 50%;
  background: #f5f5f5;
  position: relative;
  z-index: 1;
  border: 5px solid white;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.avatar-placeholder {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--gradient-primary);
  font-size: 50px;
  color: white;
}

.expert-card h3 {
  font-size: 22px;
  margin-bottom: 5px;
  font-weight: 600;
  color: var(--dark-color);
  position: relative;
  z-index: 1;
}

.expert-title {
  color: var(--primary-color);
  font-size: 16px;
  margin-bottom: 15px;
  position: relative;
  z-index: 1;
  font-weight: 500;
}

.expert-desc {
  color: #666;
  font-size: 14px;
  line-height: 1.6;
  position: relative;
  z-index: 1;
}

/* 联系我们部分样式优化 */
.contact-section {
  background: var(--gradient-primary);
  color: white;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.contact-section:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('data:image/svg+xml;utf8,<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><circle cx="50" cy="50" r="40" stroke="white" stroke-width="1" fill="none" opacity="0.2"/></svg>');
  background-size: 100px 100px;
  opacity: 0.1;
}

.contact-section h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 15px;
  text-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
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
  margin-top: 40px;
}

.contact-buttons .btn {
  margin: 0 10px;
  padding: 15px 40px;
  border-radius: 30px;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.btn-lg {
  padding: 15px 40px;
  font-size: 18px;
}

.contact-buttons .btn-primary {
  background: white;
  color: var(--primary-color);
}

.contact-buttons .btn-primary:hover {
  background: #f8f9fa;
  color: var(--primary-color);
  transform: translateY(-5px);
  box-shadow: 0 15px 25px rgba(0, 0, 0, 0.3);
}

.contact-buttons .btn-outline-light {
  background: transparent;
  border: 2px solid white;
  color: white;
}

.contact-buttons .btn-outline-light:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-5px);
  box-shadow: 0 15px 25px rgba(0, 0, 0, 0.3);
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
    height: 60vh;
    min-height: 500px;
  }
  
  .banner-content h1 {
    font-size: 32px;
  }
  
  .banner-content p {
    font-size: 16px;
  }
  
  .section {
    padding: 70px 0;
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

/* 动画效果优化 */
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


/* 添加一些特殊效果 */
/* 八卦图案背景 */
.bg-pattern {
  position: relative;
}

.bg-pattern:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('data:image/svg+xml;utf8,<svg width="60" height="60" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg"><circle cx="30" cy="30" r="29" stroke="%238e44ad" stroke-width="1" fill="none" opacity="0.1"/><path d="M30,30 m-15,0 a15,15 0 1,0 30,0 a15,15 0 1,0 -30,0" fill="none" stroke="%238e44ad" stroke-width="1" opacity="0.1"/></svg>');
  background-size: 60px 60px;
  opacity: 0.1;
}

/* 专家团队部分样式优化 */
.expert-card {
  background: white;
  border-radius: 15px;
  padding: 40px 30px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  height: 100%;
  margin-bottom: 30px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.expert-card:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 120px;
  background: var(--gradient-primary);
  opacity: 0.1;
  z-index: 0;
}

.expert-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.expert-avatar {
  width: 120px;
  height: 120px;
  margin: 0 auto 20px;
  overflow: hidden;
  border-radius: 50%;
  background: #f5f5f5;
  position: relative;
  z-index: 1;
  border: 5px solid white;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.avatar-placeholder {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  font-size: 50px;
  color: white;
}

.expert-card h3 {
  font-size: 22px;
  margin-bottom: 5px;
  font-weight: 600;
  color: #2c3e50;
  position: relative;
  z-index: 1;
}

.expert-title {
  color: #8e44ad;
  font-size: 16px;
  margin-bottom: 15px;
  position: relative;
  z-index: 1;
  font-weight: 500;
}

.expert-desc {
  color: #666;
  font-size: 14px;
  line-height: 1.6;
  position: relative;
  z-index: 1;
}

/* 联系我们部分样式优化 */
.contact-section {
  background: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  color: white;
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

.contact-section:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('data:image/svg+xml;utf8,<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><circle cx="50" cy="50" r="40" stroke="white" stroke-width="1" fill="none" opacity="0.2"/></svg>');
  background-size: 100px 100px;
  opacity: 0.1;
}

.contact-section h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 15px;
  text-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
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
  margin-top: 40px;
}

.contact-buttons .btn {
  margin: 0 10px;
  padding: 15px 40px;
  border-radius: 30px;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.contact-buttons .btn-primary {
  background: white;
  color: #8e44ad;
  border: none;
}

.contact-buttons .btn-primary:hover {
  background: #f8f9fa;
  color: #8e44ad;
  transform: translateY(-5px);
  box-shadow: 0 15px 25px rgba(0, 0, 0, 0.3);
}

.contact-buttons .btn-outline-light {
  background: transparent;
  border: 2px solid white;
  color: white;
}

.contact-buttons .btn-outline-light:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-5px);
  box-shadow: 0 15px 25px rgba(0, 0, 0, 0.3);
}

/* 添加传统元素装饰 */
.traditional-decoration {
  position: absolute;
  width: 200px;
  height: 200px;
  background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><circle cx="50" cy="50" r="50" fill="white" opacity="0.05"/><circle cx="50" cy="50" r="25" fill="white" opacity="0.05"/><circle cx="50" cy="50" r="12.5" fill="white" opacity="0.05"/></svg>');
  background-size: contain;
  opacity: 0.2;
  z-index: 0;
}

.decoration-top-right {
  top: -50px;
  right: -50px;
}

.decoration-bottom-left {
  bottom: -50px;
  left: -50px;
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
  
  .contact-section {
    padding: 80px 0;
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
    padding: 70px 0;
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
  
  .contact-buttons .btn {
    display: block;
    width: 80%;
    margin: 10px auto;
  }
}

@media (max-width: 480px) {
  .banner-content h1 {
    font-size: 28px;
  }
  
  .section-header h2 {
    font-size: 26px;
  }
  
  .expert-card {
    padding: 30px 20px;
  }
  
  .expert-avatar {
    width: 100px;
    height: 100px;
  }
}

/* 添加一些特殊效果 - 八卦图案背景 */
.bg-bagua {
  position: relative;
}

.bg-bagua:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('data:image/svg+xml;utf8,<svg width="200" height="200" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg"><circle cx="100" cy="100" r="98" stroke="%238e44ad" stroke-width="1" fill="none" opacity="0.1"/><circle cx="100" cy="100" r="50" fill="white" opacity="0.05"/><circle cx="100" cy="50" r="25" fill="black" opacity="0.05"/><circle cx="100" cy="150" r="25" fill="black" opacity="0.05"/><circle cx="100" cy="50" r="12.5" fill="white" opacity="0.05"/><circle cx="100" cy="150" r="12.5" fill="white" opacity="0.05"/></svg>');
  background-size: 200px 200px;
  opacity: 0.05;
  z-index: 0;
}

/* 添加五行元素图标 */
.wuxing-icons {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 0;
  opacity: 0.05;
  pointer-events: none;
}

.wuxing-icon {
  position: absolute;
  font-size: 40px;
  color: #8e44ad;
}

.wuxing-icon.jin {
  top: 10%;
  right: 10%;
}

.wuxing-icon.mu {
  top: 20%;
  left: 15%;
}

.wuxing-icon.shui {
  bottom: 15%;
  right: 20%;
}

.wuxing-icon.huo {
  bottom: 25%;
  left: 10%;
}

.wuxing-icon.tu {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

/* 添加动画效果 */
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}

.float-animation {
  animation: float 6s ease-in-out infinite;
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.rotate-animation {
  animation: rotate 20s linear infinite;
}

/* 添加现代科技感元素 */
.tech-particle {
  position: absolute;
  width: 5px;
  height: 5px;
  background: rgba(52, 152, 219, 0.5);
  border-radius: 50%;
}

.tech-line {
  position: absolute;
  height: 1px;
  background: linear-gradient(90deg, rgba(52, 152, 219, 0), rgba(52, 152, 219, 0.5), rgba(52, 152, 219, 0));
}

/* 自定义滚动条 */
::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(135deg, #7d3c98 0%, #2980b9 100%);
}

/* 添加CSS变量 - 在样式顶部添加 */
:root {
  --primary-color: #8e44ad; /* 紫色：代表神秘、智慧 */
  --secondary-color: #3498db; /* 蓝色：代表科技、现代 */
  --accent-color: #f39c12; /* 金色：代表传统、尊贵 */
  --dark-color: #2c3e50; /* 深蓝灰：稳重 */
  --light-color: #f8f9fa; /* 浅灰：现代感 */
  --gradient-primary: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  --gradient-secondary: linear-gradient(135deg, #f39c12 0%, #e74c3c 100%);
}

.mission-section {
  padding: 100px 0;
  background: linear-gradient(135deg, rgba(142, 68, 173, 0.05) 0%, rgba(52, 152, 219, 0.05) 100%);
  position: relative;
  overflow: hidden;
}

.mission-section:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('data:image/svg+xml;utf8,<svg width="40" height="40" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg"><path d="M20 0 L40 20 L20 40 L0 20 Z" fill="none" stroke="%238e44ad" stroke-opacity="0.05" stroke-width="1"/></svg>');
  background-size: 40px 40px;
  opacity: 0.5;
}

.mission-content {
  position: relative;
  z-index: 2;
}

.mission-header h2 {
  font-size: 36px;
  font-weight: 700;
  color: var(--dark-color);
  margin-bottom: 20px;
}

.divider {
  width: 80px;
  height: 3px;
  background: var(--gradient-primary);
  margin: 0 auto 40px;
  border-radius: 3px;
}

.mission-quote {
  text-align: center;
  margin: 30px auto;
  max-width: 800px;
  position: relative;
  padding: 20px 0;
}

.quote-mark {
  font-size: 80px;
  font-family: 'Georgia', serif;
  color: var(--primary-color);
  opacity: 0.2;
  position: absolute;
  top: -20px;
  left: -20px;
  line-height: 1;
}

.quote-mark.closing {
  left: auto;
  right: -20px;
  top: auto;
  bottom: -60px;
}

.mission-quote p {
  font-size: 28px;
  font-weight: 600;
  color: var(--primary-color);
  line-height: 1.4;
}

.mission-text {
  max-width: 900px;
  margin: 0 auto 40px;
  text-align: center;
}

.mission-text p {
  font-size: 18px;
  line-height: 1.8;
  color: #555;
  margin-bottom: 20px;
}

.mission-values {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 50px;
}

.value-item {
  text-align: center;
  padding: 20px;
  margin: 0 15px 30px;
  flex: 0 0 180px;
  transition: all 0.3s ease;
}

.value-item:hover {
  transform: translateY(-10px);
}

.value-icon {
  width: 80px;
  height: 80px;
  line-height: 80px;
  border-radius: 50%;
  background: white;
  margin: 0 auto 15px;
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.value-item:hover .value-icon {
  background: var(--gradient-primary);
}

.value-icon i {
  font-size: 30px;
  color: var(--primary-color);
  transition: all 0.3s ease;
}

.value-item:hover .value-icon i {
  color: white;
}

.value-item h4 {
  font-size: 18px;
  font-weight: 600;
  color: var(--dark-color);
  margin: 0;
}

/* 响应式调整 */
@media (max-width: 768px) {
  .mission-quote p {
    font-size: 22px;
  }
  
  .mission-text p {
    font-size: 16px;
  }
  
  .value-item {
    flex: 0 0 140px;
    margin: 0 10px 20px;
  }
}
</style>

