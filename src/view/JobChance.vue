<template>
  <div id="Partners">
    <!-- 页面banner -->
    <div class="banner container-fluid text-center">
      <div class="banner-overlay">
        <h1 class="wow fadeInUp">合作伙伴</h1>
        <p class="wow fadeInUp" data-wow-delay="0.2s">携手共创未来，共同探索命运科学的无限可能</p>
      </div>
    </div>

    <!-- 合作伙伴展示区域 -->
    <div class="partners-section">
      <div class="container">
        <!-- 学术机构 -->
        <div class="partner-category wow fadeInUp">
          <div class="section-header text-center">
            <h2>学术机构</h2>
            <div class="divider"></div>
            <p class="section-subtitle">与顶尖学术机构合作，推动命运科学理论研究</p>
          </div>
          
          <div class="partners-grid">
            <div class="partner-item wow fadeInUp" data-wow-delay="0.1s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="北京大学" onerror="this.src='https://via.placeholder.com/200x100?text=北京大学'">
              </div>
              <h3>北京大学</h3>
              <p>生命科学研究中心</p>
            </div>
            
            <div class="partner-item wow fadeInUp" data-wow-delay="0.2s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="清华大学" onerror="this.src='https://via.placeholder.com/200x100?text=清华大学'">
              </div>
              <h3>清华大学</h3>
              <p>人工智能研究院</p>
            </div>
            
            <div class="partner-item wow fadeInUp" data-wow-delay="0.3s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="中国科学院" onerror="this.src='https://via.placeholder.com/200x100?text=中国科学院'">
              </div>
              <h3>中国科学院</h3>
              <p>心理研究所</p>
            </div>
          </div>
        </div>
        
        <!-- 科技企业 -->
        <div class="partner-category wow fadeInUp">
          <div class="section-header text-center">
            <h2>科技企业</h2>
            <div class="divider"></div>
            <p class="section-subtitle">与领先科技企业合作，开发智能命运分析系统</p>
          </div>
          
          <div class="partners-grid">
            <div class="partner-item wow fadeInUp" data-wow-delay="0.1s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="腾讯" onerror="this.src='https://via.placeholder.com/200x100?text=腾讯'">
              </div>
              <h3>腾讯</h3>
              <p>AI实验室</p>
            </div>
            
            <div class="partner-item wow fadeInUp" data-wow-delay="0.2s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="阿里巴巴" onerror="this.src='https://via.placeholder.com/200x100?text=阿里巴巴'">
              </div>
              <h3>阿里巴巴</h3>
              <p>达摩院</p>
            </div>
            
            <div class="partner-item wow fadeInUp" data-wow-delay="0.3s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="华为" onerror="this.src='https://via.placeholder.com/200x100?text=华为'">
              </div>
              <h3>华为</h3>
              <p>研究院</p>
            </div>
            
            <div class="partner-item wow fadeInUp" data-wow-delay="0.4s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="百度" onerror="this.src='https://via.placeholder.com/200x100?text=百度'">
              </div>
              <h3>百度</h3>
              <p>深度学习实验室</p>
            </div>
          </div>
        </div>
        
        <!-- 传统文化机构 -->
        <div class="partner-category wow fadeInUp">
          <div class="section-header text-center">
            <h2>传统文化机构</h2>
            <div class="divider"></div>
            <p class="section-subtitle">与传统文化机构合作，传承古老智慧</p>
          </div>
          
          <div class="partners-grid">
            <div class="partner-item wow fadeInUp" data-wow-delay="0.1s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="中国道教协会" onerror="this.src='https://via.placeholder.com/200x100?text=中国道教协会'">
              </div>
              <h3>中国道教协会</h3>
              <p>传统文化研究中心</p>
            </div>
            
            <div class="partner-item wow fadeInUp" data-wow-delay="0.2s">
              <div class="partner-logo">
                <img src="../assets/img/partners/weixin.png" alt="国学研究院" onerror="this.src='https://via.placeholder.com/200x100?text=国学研究院'">
              </div>
              <h3>国学研究院</h3>
              <p>易学研究中心</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- 合作邀请 -->
    <div class="cooperation-section">
      <div class="container">
        <div class="cooperation-content text-center wow fadeInUp">
          <h2>诚邀合作</h2>
          <p>我们期待与更多志同道合的机构和企业建立合作关系，共同推动命运科学的发展与应用</p>
          <button class="btn btn-primary btn-lg">联系我们</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { WOW } from 'wowjs';

export default {
  name: "Partners",
  data() {
    return {
      // 这里可以添加合作伙伴数据，未来可以从API获取
      partners: {
        academic: [
          { name: '北京大学', department: '生命科学研究中心', logo: 'weixin.png' },
          { name: '清华大学', department: '人工智能研究院', logo: 'weixin.png' },
          { name: '中国科学院', department: '心理研究所', logo: 'weixin.png' }
        ],
        tech: [
          { name: '腾讯', department: 'AI实验室', logo: 'weixin.png' },
          { name: '阿里巴巴', department: '达摩院', logo: 'weixin.png' },
          { name: '华为', department: '研究院', logo: 'weixin.png' },
          { name: '百度', department: '深度学习实验室', logo: 'weixin.png' }
        ],
        culture: [
          { name: '中国道教协会', department: '传统文化研究中心', logo: 'weixin.png' },
          { name: '国学研究院', department: '易学研究中心', logo: 'weixin.png' }
        ]
      }
    };
  },
  mounted() {
    // 初始化WOW.js动画
    new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: false
    }).init();
  },
  methods: {
    // 可以添加方法，如联系我们按钮的点击事件
    contactUs() {
      // 实现联系功能
      this.$router.push('/contactus');
    }
  }
};
</script>

<style scoped>
/* 主题颜色变量 */
:root {
  --primary-color: #8e44ad; /* 紫色：代表神秘、智慧 */
  --secondary-color: #3498db; /* 蓝色：代表科技、现代 */
  --accent-color: #f39c12; /* 金色：代表传统、尊贵 */
  --dark-color: #2c3e50; /* 深蓝灰：稳重 */
  --light-color: #f8f9fa; /* 浅灰：现代感 */
  --gradient-primary: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
}

/* Banner样式 */
.banner {
  position: relative;
  color: #fff;
  height: 300px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 0;
}

.banner-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(44, 62, 80, 0.7);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 20px;
}

.banner h1 {
  font-size: 48px;
  font-weight: 700;
  margin-bottom: 15px;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
}

.banner p {
  font-size: 20px;
  max-width: 700px;
  margin: 0 auto;
  opacity: 0.9;
}

/* 合作伙伴部分样式 */
.partners-section {
  padding: 80px 0;
  background: #f8f9fa;
}

.partner-category {
  margin-bottom: 80px;
}

.section-header {
  margin-bottom: 50px;
}

.section-header h2 {
  font-size: 36px;
  font-weight: 700;
  color: #2c3e50;
  margin-bottom: 15px;
}

.divider {
  width: 80px;
  height: 3px;
  background: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  margin: 0 auto 20px;
  border-radius: 3px;
}

.section-subtitle {
  font-size: 18px;
  color: #666;
  max-width: 700px;
  margin: 0 auto;
}

.partners-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
}

.partner-item {
  background: white;
  border-radius: 10px;
  padding: 30px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  width: 250px;
  text-align: center;
}

.partner-item:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.partner-logo {
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
}

.partner-logo img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.partner-item h3 {
  font-size: 20px;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 5px;
}

.partner-item p {
  color: #666;
  font-size: 14px;
}

/* 合作邀请部分样式 */
.cooperation-section {
  padding: 100px 0;
  background: linear-gradient(135deg, #8e44ad 0%, #3498db 100%);
  color: white;
  position: relative;
  overflow: hidden;
}

.cooperation-section:before {
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

.cooperation-content {
  position: relative;
  z-index: 1;
}

.cooperation-content h2 {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 20px;
  text-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.cooperation-content p {
  font-size: 18px;
  max-width: 700px;
  margin: 0 auto 30px;
  opacity: 0.9;
}

.btn-primary {
  background: white;
  color: #8e44ad;
  border: none;
  padding: 12px 30px;
  border-radius: 30px;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.btn-primary:hover {
  background: #f8f9fa;
  color: #8e44ad;
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
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

/* 响应式调整 */
@media (max-width: 991px) {
  .banner {
    height: 250px;
  }
  
  .banner h1 {
    font-size: 36px;
  }
  
  .banner p {
    font-size: 18px;
  }
  
  .section-header h2 {
    font-size: 30px;
  }
  
  .partners-grid {
    gap: 20px;
  }
  
  .partner-item {
    width: 220px;
    padding: 25px;
  }
}

@media (max-width: 767px) {
  .banner {
    height: 200px;
  }
  
  .banner h1 {
    font-size: 30px;
  }
  
  .banner p {
    font-size: 16px;
  }
  
  .partners-section {
    padding: 60px 0;
  }
  
  .partner-category {
    margin-bottom: 60px;
  }
  
  .section-header {
    margin-bottom: 30px;
  }
  
  .section-header h2 {
    font-size: 26px;
  }
  
  .partner-item {
    width: 100%;
    max-width: 280px;
  }
  
  .cooperation-section {
    padding: 70px 0;
  }
  
  .cooperation-content h2 {
    font-size: 30px;
  }
  
  .cooperation-content p {
    font-size: 16px;
  }
}
</style>

