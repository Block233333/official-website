<template>
  <div id="CompanyIntroduction">
    <!-- 页面顶部横幅 -->
    <div class="banner container-fluid">
      <div class="banner-overlay"></div>
      <div class="banner-content">
        <h1 class="wow fadeInUp">关于我们</h1>
        <div class="banner-divider wow fadeInUp" data-wow-delay="0.2s"></div>
        <p class="wow fadeInUp" data-wow-delay="0.4s">传统智慧与现代科技的完美融合</p>
      </div>
    </div>
    
    <!-- 公司简介部分 -->
    <section class="company-intro section">
      <div class="container">
        <div class="section-header text-center wow fadeInUp">
          <span class="section-subtitle">企业简介</span>
          <h2 class="section-title">厦门知命者文化产业有限公司</h2>
          <div class="section-divider center-divider"></div>
        </div>
        
        <div class="row company-intro-container align-items-center">
          <div class="col-xs-12 col-sm-12 col-md-6 wow fadeInLeft">
            <div class="company-image">
              <img class="img-responsive" src="@/assets/img/Designer.jpeg" alt="知命者文化">
              <div class="image-overlay">
                <div class="overlay-content">
                  <h3>知命者文化</h3>
                  <p>创立于2023年</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-xs-12 col-sm-12 col-md-6 wow fadeInRight">
            <div class="company-content">
              <div class="content-block">
                <h3 class="block-title">我们的使命</h3>
                <p class="text-justify">知命者，是一家以传统智慧与现代科技融合为核心的创新服务平台，汇聚了精通玄学文化、生命科学、环境科学及天文学等领域的顶尖专家与学者，致力于为个人与企业提供命运科学探究、生命状态分析、运程预测优化及人生规划指导等全方位解决方案。我们通过自主研发的智能提示系统，结合四柱八字、紫微斗数、中医养生等传统智慧与人工智能技术，帮助用户改善生命状态、调节时空环境，助力突破命运障碍，成就更加畅通美好的人生旅程。</p>
              </div>
              <div class="content-block">
                <h3 class="block-title">我们的服务</h3>
                <p class="text-justify">我们的服务涵盖个人命运改进咨询、企业环境能量优化、传统文化传承合作等领域，客户遍及教育、医疗、文化产业、大健康行业及传统文化机构，并与国学研究院、生命科学研究所、环境工程机构等建立了深度合作。依托严谨的科学态度与深厚的文化底蕴，我们为每一位用户制定个性化方案，成功协助数千人优化生命轨迹，重塑人生价值。知命者始终以"利人利己"为根基，以创新科技赋能传统智慧，为中华文化的全球传播与时代焕新开辟全新道路，让命运科学惠及众生。</p>
              </div>
              <div class="company-values">
                <div class="value-item wow fadeInUp">
                  <div class="value-icon">
                    <i class="fa fa-balance-scale"></i>
                  </div>
                  <div class="value-content">
                    <h4>传统与现代融合</h4>
                    <p>结合古老智慧与前沿科技</p>
                  </div>
                </div>
                <div class="value-item wow fadeInUp" data-wow-delay="0.2s">
                  <div class="value-icon">
                    <i class="fa fa-users"></i>
                  </div>
                  <div class="value-content">
                    <h4>专业团队支持</h4>
                    <p>顶尖专家提供全方位指导</p>
                  </div>
                </div>
                <div class="value-item wow fadeInUp" data-wow-delay="0.4s">
                  <div class="value-icon">
                    <i class="fa fa-lightbulb-o"></i>
                  </div>
                  <div class="value-content">
                    <h4>创新解决方案</h4>
                    <p>个性化命运优化服务</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { WOW } from 'wowjs';
export default {
  name: 'CompanyIntroduction',
  data(){
    return{
      
    }
  },
  mounted(){
    var wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 100,
      mobile: true,
      live: true
    });
    wow.init();
  }
}
</script>

<style scoped>
/* 全局样式 */
#CompanyIntroduction {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  color: #333;
  line-height: 1.6;
}

.section {
  padding: 100px 0;
}

/* 章节标题样式 */
.section-header {
  margin-bottom: 60px;
}

.section-subtitle {
  display: inline-block;
  font-size: 16px;
  color: #3498db;
  font-weight: 500;
  margin-bottom: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.section-title {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 20px;
  color: #2c3e50;
}

.section-divider {
  width: 80px;
  height: 3px;
  background: linear-gradient(to right, #3498db, #2c3e50);
  margin-bottom: 20px;
}

.center-divider {
  margin: 0 auto 20px;
}

/* 横幅样式 */
.banner {
  position: relative;
  height: 400px;
  background-image: url('../assets/img/banner1.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #fff;
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

/* 公司简介样式 */
.company-intro-container {
  margin-top: 40px;
}

.company-image {
  position: relative;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
  margin-bottom: 30px;
}

.company-image img {
  width: 100%;
  transition: transform 0.5s ease;
}

.company-image:hover img {
  transform: scale(1.05);
}

.image-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
  padding: 20px;
  color: #fff;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.company-image:hover .image-overlay {
  opacity: 1;
}

.overlay-content h3 {
  font-size: 24px;
  margin-bottom: 5px;
}

.overlay-content p {
  font-size: 14px;
  margin: 0;
}

.company-content {
  padding: 0 20px;
}

.content-block {
  margin-bottom: 30px;
}

.block-title {
  font-size: 24px;
  font-weight: 600;
  color: #2c3e50;
  margin-bottom: 15px;
  position: relative;
  padding-left: 15px;
}

.block-title:before {
  content: '';
  position: absolute;
  left: 0;
  top: 8px;
  width: 5px;
  height: 20px;
  background-color: #3498db;
}

.text-justify {
  text-align: justify;
  font-size: 16px;
  line-height: 1.8;
  color: #555;
  margin-bottom: 20px;
}

/* 公司价值观样式 */
.company-values {
  display: flex;
  flex-wrap: wrap;
  margin-top: 40px;
}

.value-item {
  display: flex;
  align-items: flex-start;
  margin-bottom: 20px;
  width: 100%;
}

.value-icon {
  width: 50px;
  height: 50px;
  background-color: rgba(52, 152, 219, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 15px;
  flex-shrink: 0;
}

.value-icon i {
  font-size: 24px;
  color: #3498db;
}

.value-content h4 {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 5px;
  color: #2c3e50;
}

.value-content p {
  font-size: 14px;
  color: #666;
  margin: 0;
}

/* 响应式调整 */
@media (max-width: 991px) {
  .section {
    padding: 80px 0;
  }
  
  .section-title {
    font-size: 32px;
  }
  
  .banner {
    height: 300px;
  }
  
  .banner-content h1 {
    font-size: 36px;
  }
  
  .banner-content p {
    font-size: 18px;
  }
  
  .company-content {
    padding: 0;
    margin-top: 30px;
  }
}

@media (max-width: 767px) {
  .section {
    padding: 60px 0;
  }
  
  .section-title {
    font-size: 28px;
  }
  
  .banner {
    height: 250px;
  }
  
  .banner-content h1 {
    font-size: 30px;
  }
  
  .banner-content p {
    font-size: 16px;
  }
  
  .block-title {
    font-size: 22px;
  }
  
  .text-justify {
    font-size: 15px;
    line-height: 1.7;
  }
}

@media (max-width: 480px) {
  .section {
    padding: 40px 0;
  }
  
  .banner {
    height: 200px;
  }
  
  .banner-content h1 {
    font-size: 24px;
  }
  
  .banner-content p {
    font-size: 14px;
  }
  
  .section-title {
    font-size: 24px;
  }
}

/* 动画效果 */
.wow {
  visibility: hidden;
}
</style>

