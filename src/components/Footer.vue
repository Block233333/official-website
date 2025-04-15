<template>
  <div id="footer" class="container-fluid">
    <div class="footer-content">
      <div class="row">
        <div class="col-md-4 col-sm-12 footer-brand">
          <div class="logo">
            <img src="@/assets/img/logo_white.png" alt="logo图">
          </div>
          <p class="title">知命者文化产业有限公司</p>
          <p class="slogan">传统智慧与现代科技的完美融合</p>
        </div>
        
        <div class="col-md-4 col-sm-12 footer-contact">
          <h4>联系方式</h4>
          <p><i class="glyphicon glyphicon-map-marker"></i> 香港鰂魚涌華蘭路20號華蘭中心7樓7室</p>
          <p><i class="glyphicon glyphicon-phone"></i> +852 2814 1083</p>
          <p><i class="glyphicon glyphicon-envelope"></i> contact@zhimingzhe.com</p>
        </div>
        
        <div class="col-md-4 col-sm-12 footer-links">
          <h4>快速链接</h4>
          <ul>
            <li><a href="/">首页</a></li>
            <li><a href="/service">公司服务</a></li>
            <li><a href="/companyintroduction">公司介绍</a></li>
            <li><a href="/contactus">联系我们</a></li>
          </ul>
          <!-- 修改社交链接部分 -->
          <div class="social-links">
            <div class="social-item">
              <a href="#" class="social-link" title="微信" @click.prevent="showQRCode('weixin')">
                <img src="@/assets/img/weixin.png" alt="微信" class="social-icon">
              </a>
              <div class="qr-popup" v-if="activeQR === 'weixin'">
                <img src="@/assets/img/wechat.png" alt="微信二维码" class="qr-code">
              </div>
            </div>
            <div class="social-item">
              <a href="#" class="social-link" title="微博" @click.prevent="showQRCode('weibo')">
                <img src="@/assets/img/weibo.png" alt="微博" class="social-icon">
              </a>
              <div class="qr-popup" v-if="activeQR === 'weibo'">
                <img src="@/assets/img/wechat.png" alt="微博二维码" class="qr-code">
              </div>
            </div>
            <div class="social-item">
              <a href="#" class="social-link" title="小红书" @click.prevent="showQRCode('xiaohongshu')">
                <img src="@/assets/img/rednote.png" alt="小红书" class="social-icon">
              </a>
              <div class="qr-popup" v-if="activeQR === 'xiaohongshu'">
                <img src="@/assets/img/wechat.png" alt="小红书二维码" class="qr-code">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <p class="copy">Copyright &copy; 2018 - {{ new Date().getFullYear() }} 知命者文化产业有限公司 版权所有</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      activeQR: null
    };
  },
  methods: {
    showQRCode(type) {
      this.activeQR = this.activeQR === type ? null : type;
    },
    handleClickOutside(e) {
      if (!e.target.closest('.social-item')) {
        this.activeQR = null;
      }
    }
  },
  mounted() {
    document.addEventListener('click', this.handleClickOutside);
  },
  beforeDestroy() {
    document.removeEventListener('click', this.handleClickOutside);
  }
};
</script>

<style scoped>
#footer {
  width: 100%;
  color: #fff;
  background: #2c3e50;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.footer-content {
  padding: 60px 10% 40px;
}

.footer-brand .logo {
  width: 120px;
  height: 60px;
  margin-bottom: 20px;
}

.footer-brand .logo img {
  max-width: 100%;
  height: auto;
}

.footer-brand .title {
  font-size: 22px;
  font-weight: 600;
  margin-bottom: 10px;
}

.footer-brand .slogan {
  color: #bdc3c7;
  font-size: 14px;
}

.footer-contact h4,
.footer-links h4 {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 20px;
  position: relative;
  padding-bottom: 10px;
}

.footer-contact h4:after,
.footer-links h4:after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 50px;
  height: 2px;
  background: #3498db;
}

.footer-contact p {
  color: #bdc3c7;
  margin-bottom: 10px;
  font-size: 14px;
}

.footer-contact i {
  margin-right: 10px;
  color: #3498db;
}

.footer-links ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links ul li {
  margin-bottom: 10px;
}

.footer-links ul li a {
  color: #bdc3c7;
  text-decoration: none;
  transition: all 0.3s ease;
}

.footer-links ul li a:hover {
  color: #3498db;
  padding-left: 5px;
}

/* 修改社交链接样式 */
.social-links {
  margin-top: 20px;
  display: flex;
}

.social-item {
  position: relative;
  margin-right: 15px;
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 36px;
  height: 36px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  transition: all 0.3s ease;
}

.social-link:hover {
  background: #3498db;
  transform: translateY(-3px);
}

.social-icon {
  width: 20px;
  height: 20px;
  object-fit: contain;
}

.qr-popup {
  position: absolute;
  bottom: 100%;
  left: 50%;
  transform: translateX(-50%);
  margin-bottom: 10px;
  padding: 10px;
  background: white;
  border-radius: 8px;
  box-shadow: 0 3px 15px rgba(0, 0, 0, 0.2);
  z-index: 1000;
}

.qr-popup::after {
  content: '';
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border-width: 8px;
  border-style: solid;
  border-color: white transparent transparent transparent;
}

.qr-code {
  width: 120px;
  height: 120px;
  display: block;
}

.footer-bottom {
  background: #1a252f;
  padding: 20px 0;
  text-align: center;
}

.copy {
  color: #bdc3c7;
  font-size: 14px;
  margin: 0;
}

@media screen and (max-width: 997px) {
  .footer-content {
    padding: 40px 5% 20px;
  }
  
  .footer-brand, .footer-contact, .footer-links {
    text-align: center;
    margin-bottom: 30px;
  }
  
  .footer-brand .logo {
    margin: 0 auto 20px;
  }
  
  .footer-contact h4:after,
  .footer-links h4:after {
    left: 50%;
    transform: translateX(-50%);
  }
  
  .social-links {
    justify-content: center;
  }
}
</style>

