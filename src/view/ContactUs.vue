<template>
  <div id="ContactUs">
    <!-- 页面顶部横幅 -->
    <div class="banner container-fluid">
      <div class="banner-overlay"></div>
      <div class="banner-content">
        <h1 class="wow fadeInUp">联系我们</h1>
        <div class="banner-divider wow fadeInUp" data-wow-delay="0.2s"></div>
        <p class="wow fadeInUp" data-wow-delay="0.4s">我们期待与您沟通，共同探索命运的奥秘</p>
      </div>
    </div>
    
    <!-- 联系信息与表单部分 -->
    <section class="contact-section section">
      <div class="container">
        <div class="row">
          <!-- 联系信息部分 -->
          <div class="col-md-4 col-sm-12 wow fadeInLeft">
            <div class="contact-info-card">
              <h3 class="info-title">联系方式</h3>
              <div class="info-item">
                <div class="info-icon">
                  <i class="fa fa-map-marker"></i>
                </div>
                <div class="info-content">
                  <h4>公司地址</h4>
                  <p>香港鰂魚涌華蘭路20號華蘭中心7樓7室</p>
                </div>
              </div>
              <div class="info-item">
                <div class="info-icon">
                  <i class="fa fa-phone"></i>
                </div>
                <div class="info-content">
                  <h4>联系电话</h4>
                  <p>+852 2814 1083</p>
                </div>
              </div>
              <div class="info-item">
                <div class="info-icon">
                  <i class="fa fa-envelope"></i>
                </div>
                <div class="info-content">
                  <h4>电子邮箱</h4>
                  <p>contact@zhimingzhe.com</p>
                </div>
              </div>
              <div class="info-item">
                <div class="info-icon">
                  <i class="fa fa-clock-o"></i>
                </div>
                <div class="info-content">
                  <h4>工作时间</h4>
                  <p>周一至周五: 9:00 - 18:00</p>
                  <p>周六至周日: 10:00 - 16:00</p>
                </div>
              </div>
              <div class="social-links">
                <a href="#" class="social-link" title="微信">
                  <img src="@/assets/img/weixin.png" alt="微信" class="social-icon">
                </a>
                <a href="#" class="social-link" title="微博">
                  <img src="@/assets/img/weibo.png" alt="微博" class="social-icon">
                </a>
                <a href="#" class="social-link" title="小红书">
                  <img src="@/assets/img/rednote.png" alt="小红书" class="social-icon">
                </a>
              </div>
            </div>
          </div>
          
          <!-- 联系表单部分 -->
          <div class="col-md-8 col-sm-12 wow fadeInRight">
            <div class="contact-form-card">
              <h3 class="form-title">发送消息</h3>
              <p class="form-description">如有任何疑问或需求，请填写以下表单，我们将尽快与您联系</p>
              
              <form class="contact-form" @submit.prevent="submitForm">
                <div class="row">
                  <div class="col-md-6">
                    <div class="form-group">
                      <label for="name">您的姓名 <span class="required">*</span></label>
                      <input 
                        type="text" 
                        class="form-control" 
                        id="name" 
                        v-model="formData.name" 
                        placeholder="请输入您的姓名"
                        required
                      >
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="form-group">
                      <label for="email">电子邮箱 <span class="required">*</span></label>
                      <input 
                        type="email" 
                        class="form-control" 
                        id="email" 
                        v-model="formData.email" 
                        placeholder="请输入您的邮箱"
                        required
                      >
                    </div>
                  </div>
                </div>
                
                <div class="row">
                  <div class="col-md-6">
                    <div class="form-group">
                      <label for="tel">联系电话</label>
                      <input 
                        type="tel" 
                        class="form-control" 
                        id="tel" 
                        v-model="formData.tel" 
                        placeholder="请输入您的电话"
                      >
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="form-group">
                      <label for="subject">咨询主题</label>
                      <select class="form-control" id="subject" v-model="formData.subject">
                        <option value="">请选择咨询主题</option>
                        <option value="命运分析">命运分析</option>
                        <option value="生命优化">生命优化</option>
                        <option value="企业合作">企业合作</option>
                        <option value="其他咨询">其他咨询</option>
                      </select>
                    </div>
                  </div>
                </div>
                
                <div class="form-group">
                  <label for="content">咨询内容 <span class="required">*</span></label>
                  <textarea 
                    class="form-control" 
                    id="content" 
                    v-model="formData.content" 
                    rows="6" 
                    placeholder="请详细描述您的需求或问题"
                    required
                  ></textarea>
                </div>
                
                <div class="form-group">
                  <div class="checkbox">
                    <label>
                      <input type="checkbox" v-model="formData.agreement" required> 我同意贵公司收集和使用我的个人信息用于回复咨询
                    </label>
                  </div>
                </div>
                
                <div class="form-group">
                  <button 
                    type="submit" 
                    class="btn btn-primary btn-lg btn-block"
                    :disabled="isSubmitting"
                  >
                    {{ isSubmitting ? '提交中...' : '提交咨询' }}
                  </button>
                </div>
                
                <div v-if="submitMessage" :class="['alert', submitStatus ? 'alert-success' : 'alert-danger']">
                  {{ submitMessage }}
                </div>
              </form>
            </div>
          </div>
        </div>
        
        <!-- 地图部分 -->
        <div class="row map-section wow fadeInUp">
          <div class="col-md-12">
            <h3 class="map-title">我们的位置</h3>
            <div id="map" class="map-container"></div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { WOW } from 'wowjs'
import BMap from "BMap";
import axios from 'axios'; // 需要安装axios: npm install axios

export default {
  name: "ContactUs",
  data() {
    return {
      formData: {
        name: '',
        email: '',
        tel: '',
        subject: '',
        content: '',
        agreement: false,
        timestamp: ''
      },
      isSubmitting: false,
      submitMessage: '',
      submitStatus: false
    };
  },
  methods: {
    // 提交表单方法
    submitForm() {
      // 表单验证
      if (!this.formData.name || !this.formData.email || !this.formData.content) {
        this.submitMessage = '请填写必填字段';
        this.submitStatus = false;
        return;
      }
      
      if (!this.formData.agreement) {
        this.submitMessage = '请同意个人信息收集声明';
        this.submitStatus = false;
        return;
      }
      
      // 设置提交状态
      this.isSubmitting = true;
      this.submitMessage = '';
      
      // 添加时间戳
      this.formData.timestamp = new Date().toISOString();
      
      // 这里将添加表单数据存储逻辑
      // 模拟提交成功
      setTimeout(() => {
        this.submitMessage = '您的咨询已成功提交，我们将尽快与您联系！';
        this.submitStatus = true;
        this.resetForm();
        this.isSubmitting = false;
      }, 1500);
    },
    
    // 重置表单
    resetForm() {
      this.formData = {
        name: '',
        email: '',
        tel: '',
        subject: '',
        content: '',
        agreement: false,
        timestamp: ''
      };
    }
  },
  mounted() {
    // 设置当前导航索引为"联系我们"
    const contactUsIndex = 6; // 联系我们在导航列表中的索引
    sessionStorage.setItem('navIndex', contactUsIndex);
    
    // 确保页面从顶部开始显示
    window.scrollTo(0, 0);
    
    // 百度地图初始化 (保持不变)
    var map = new BMap.Map("map"); // 创建地图实例
    var point = new BMap.Point(114.224683,22.290108); // 创建点坐标
    map.centerAndZoom(point, 18); // 初始化地图，设置中心点坐标和地图级别
    map.enableScrollWheelZoom(true); //开启鼠标滚轮缩放
    var marker = new BMap.Marker(point); // 创建标注
    map.addOverlay(marker); // 将标注添加到地图中
    var opts = {
      width: 50, // 信息窗口宽度
      height: 10, // 信息窗口高度
      title: "知命者文化产业有限公司" // 信息窗口标题
    };
    var infoWindow = new BMap.InfoWindow(
      "香港鰂魚涌華蘭路20號華蘭中心7樓7室",
      opts
    ); // 创建信息窗口对象
    map.openInfoWindow(infoWindow, map.getCenter()); // 打开信息窗口
    
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
#ContactUs {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  color: #333;
  line-height: 1.6;
}

.section {
  padding: 100px 0;
}

/* 横幅样式 */
.banner {
  position: relative;
  height: 350px;
  background-image: url("../assets/img/contactus_bg.jpeg");
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

/* 联系信息卡片样式 */
.contact-info-card {
  background-color: #fff;
  border-radius: 10px;
  padding: 30px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  height: 100%;
  margin-bottom: 30px;
}

.info-title {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 25px;
  color: #2c3e50;
  position: relative;
  padding-bottom: 15px;
}

.info-title:after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 50px;
  height: 3px;
  background: linear-gradient(to right, #3498db, #2c3e50);
}

.info-item {
  display: flex;
  margin-bottom: 20px;
}

.info-icon {
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

.info-icon i {
  font-size: 24px;
  color: #3498db;
}

.info-content h4 {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 5px;
  color: #2c3e50;
}

.info-content p {
  font-size: 15px;
  color: #666;
  margin-bottom: 5px;
}

/* 社交链接样式 */
.social-links {
  display: flex;
  margin-top: 30px;
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  margin-right: 15px;
  background-color: rgba(52, 152, 219, 0.1);
  border-radius: 50%;
  transition: all 0.3s ease;
}

.social-link:hover {
  background-color: #3498db;
  transform: translateY(-5px);
}

.social-icon {
  width: 20px;
  height: 20px;
  object-fit: contain;
  transition: all 0.3s ease;
}

.social-link:hover .social-icon {
  transform: scale(1.2);
}

/* 联系表单卡片样式 */
.contact-form-card {
  background-color: #fff;
  border-radius: 10px;
  padding: 30px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  height: 100%;
  margin-bottom: 30px;
}

.form-title {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 10px;
  color: #2c3e50;
  position: relative;
  padding-bottom: 15px;
}

.form-title:after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 50px;
  height: 3px;
  background: linear-gradient(to right, #3498db, #2c3e50);
}

.form-description {
  font-size: 15px;
  color: #666;
  margin-bottom: 25px;
}

.contact-form .form-group {
  margin-bottom: 20px;
}

.contact-form label {
  font-weight: 500;
  color: #2c3e50;
  margin-bottom: 8px;
  display: block;
}

.required {
  color: #e74c3c;
}

.contact-form .form-control {
  height: 45px;
  border-radius: 5px;
  border: 1px solid #ddd;
  box-shadow: none;
  transition: all 0.3s ease;
}

.contact-form .form-control:focus {
  border-color: #3498db;
  box-shadow: 0 0 8px rgba(52, 152, 219, 0.2);
}

.contact-form textarea.form-control {
  height: auto;
  resize: vertical;
}

.contact-form .btn {
  padding: 12px 30px;
  border-radius: 5px;
  font-weight: 500;
  transition: all 0.3s ease;
}

.btn-primary {
  background-color: #3498db;
  border-color: #3498db;
  color: #fff;
}

.btn-primary:hover, .btn-primary:focus {
  background-color: #2980b9;
  border-color: #2980b9;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.btn-primary:disabled {
  background-color: #95a5a6;
  border-color: #95a5a6;
}

.alert {
  margin-top: 20px;
  border-radius: 5px;
  padding: 15px;
}

.alert-success {
  background-color: #d4edda;
  color: #155724;
  border-color: #c3e6cb;
}

.alert-danger {
  background-color: #f8d7da;
  color: #721c24;
  border-color: #f5c6cb;
}

/* 地图部分样式 */
.map-section {
  margin-top: 50px;
}

.map-title {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 20px;
  color: #2c3e50;
  text-align: center;
}

.map-container {
  width: 100%;
  height: 400px;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
}

/* 响应式调整 */
@media (max-width: 991px) {
  .section {
    padding: 80px 0;
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
  
  .contact-info-card, .contact-form-card {
    margin-bottom: 30px;
  }
}

@media (max-width: 767px) {
  .section {
    padding: 60px 0;
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
  
  .map-container {
    height: 350px;
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
  
  .contact-info-card, .contact-form-card {
    padding: 20px;
  }
  
  .map-container {
    height: 300px;
  }
}

/* 动画效果 */
.wow {
  visibility: hidden;
}
</style>

