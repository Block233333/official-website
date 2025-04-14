<template>
    <div id="Service">
        <!-- 页面顶部横幅 -->
        <div class="service-banner container-fluid">
            <div class="banner-overlay"></div>
            <div class="banner-content text-center">
                <h1 class="wow fadeInUp">我们的服务</h1>
                <div class="banner-divider wow fadeInUp" data-wow-delay="0.2s"></div>
                <p class="wow fadeInUp" data-wow-delay="0.4s">传统智慧与现代科技的完美融合</p>
            </div>
        </div>
        
        <div class="container service-section">
            <div class="section-header text-center wow fadeInUp">
                <span class="section-subtitle">专业服务</span>
                <h2 class="section-title">为您提供全方位的命运科学解决方案</h2>
                <div class="section-divider center-divider"></div>
                <p class="section-description">我们汇聚了精通玄学文化、生命科学、环境科学及天文学等领域的顶尖专家与学者</p>
            </div>
            
            <div class="Service-container row">
                <div class="Service-item col-xs-12 col-sm-6 col-md-3 wow fadeInUp" 
                v-for="(item,index) in serviceList" :key="index" @click="ServiceClick(item.id)"
                :data-wow-delay="0.2 * index + 's'">
                    <div class="Service-item-wrapper">
                        <div class="Service-item-top">
                            <h4>{{item.title}}</h4>
                            <i></i>
                            <p>{{item.eng_title}}</p>
                        </div>
                        <div class="Service-item-img">
                            <img :src="item.img" alt="服务">
                            <div class="overlay">
                                <div class="overlay-content">
                                    <span>了解更多</span>
                                </div>
                            </div>
                        </div>
                        <div class="Service-item-border"></div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 服务优势部分 -->
        <div class="service-features container-fluid">
            <div class="container">
                <div class="row">
                    <div class="col-md-6 col-sm-12 wow fadeInLeft">
                        <div class="features-content">
                            <h2>为什么选择我们的服务</h2>
                            <p>知命者文化以严谨的科学态度与深厚的文化底蕴，为每一位用户制定个性化方案，成功协助数千人优化生命轨迹，重塑人生价值。</p>
                            <ul class="features-list">
                                <li><i class="fa fa-check-circle"></i> 专业团队支持，顶尖专家提供全方位指导</li>
                                <li><i class="fa fa-check-circle"></i> 传统与现代融合，结合古老智慧与前沿科技</li>
                                <li><i class="fa fa-check-circle"></i> 个性化定制方案，针对您的独特需求</li>
                                <li><i class="fa fa-check-circle"></i> 科学验证体系，确保服务效果可靠</li>
                            </ul>
                            <button class="btn btn-primary" @click="contactUs">联系我们</button>
                        </div>
                    </div>
                    <div class="col-md-6 col-sm-12 wow fadeInRight">
                        <div class="features-image">
                            <img src="@/assets/img/circle.png" alt="服务特点">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { WOW } from 'wowjs';
export default {
    name: 'Service',
    data(){
        return{
            serviceList: [
                {
                    id: 'section-1',
                    title: '命运科学探究与咨询',
                    eng_title: 'Fate Research & Consultation',
                    img: require('@/assets/img/service1.jpeg')
                },{
                    id: 'section-2',
                    title: '生命状态综合诊断',
                    eng_title: 'Comprehensive Life Diagnosis',
                    img: require('@/assets/img/service2.jpeg')
                },{
                    id: 'section-3',
                    title: '智能环境与运程优化',
                    eng_title: 'Smart Destiny Optimization',
                    img: require('@/assets/img/service3.jpeg')
                },{
                    id: 'section-4',
                    title: '导师团队定制化指导',
                    eng_title: 'Expert Mentorship Programs',
                    img: require('@/assets/img/service4.jpeg')
                }
            ]
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
    },
    methods:{
        ServiceClick(id){
            this.$router.push({
                name: 'servicedetail',
                params: {
                    id: id
                }
            })
        },
        contactUs() {
            this.$router.push({
                name: 'contactus'
            })
        }
    }
}
</script>

<style scoped>
/* 全局样式 */
#Service {
    font-family: 'Helvetica Neue', Arial, sans-serif;
    color: #333;
    line-height: 1.6;
}

/* 横幅样式 */
.service-banner {
    position: relative;
    height: 350px;
    background-image: url("../assets/img/banner_2.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #fff;
    margin-bottom: 50px;
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

/* 章节标题样式 */
.service-section {
    padding: 50px 0;
}

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

.section-description {
    font-size: 18px;
    color: #666;
    max-width: 800px;
    margin: 0 auto 40px;
}

/* 服务项目样式 */
.Service-container{
    padding: 30px 0;
}

.Service-item{
    margin-bottom: 50px;
    padding: 0 15px;
}

.Service-item-wrapper{
    cursor: pointer;
    background: #fff;
    overflow: hidden;
    position: relative;
    border-radius: 10px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
}

.Service-item-wrapper:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.Service-item-top{
    width: 100%;
    height: 120px;
    padding: 30px;
    text-align: center;
    background-color: #fff;
}

.Service-item-top h4 {
    font-size: 18px;
    font-weight: 600;
    color: #2c3e50;
    margin-bottom: 15px;
}

.Service-item-top>i{
    display: inline-block;
    width: 40px;
    height: 3px;
    background: #3498db;
    margin-bottom: 10px;
    transition: all .5s ease;
}

.Service-item-top>p{
    color: #666;
    font-size: 14px;
    opacity: 0;
    transform: translateY(10px);
    transition: all .5s ease;
}

.Service-item-img{
    width: 100%;
    height: 200px;
    overflow: hidden;
    position: relative;
}

.Service-item-img img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: all 0.5s ease;
}

.overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(52, 152, 219, 0.7);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: all 0.5s ease;
}

.overlay-content {
    color: #fff;
    text-align: center;
    transform: translateY(20px);
    transition: all 0.5s ease;
}

.overlay-content span {
    display: inline-block;
    padding: 8px 20px;
    border: 2px solid #fff;
    border-radius: 30px;
    font-size: 14px;
    font-weight: 500;
}

.Service-item-border{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    z-index: 9;
    width: 100%;
    height: 100%;
    transition: all 0.5s ease;
    border: 1px solid #3498db;
    opacity: 0;
}

.Service-item-wrapper:hover .Service-item-top > i{
    width: 60px;
}

.Service-item-wrapper:hover .Service-item-top > p{
    opacity: 1;
    transform: translateY(0);
}

.Service-item-wrapper:hover .Service-item-img > img{
    transform: scale(1.1);
}

.Service-item-wrapper:hover .overlay {
    opacity: 1;
}

.Service-item-wrapper:hover .overlay-content {
    transform: translateY(0);
}

.Service-item-wrapper:hover > .Service-item-border{
    opacity: 1;
    width: 90%;
    height: 90%;
}

/* 服务特点部分 */
.service-features {
    background-color: #f8f9fa;
    padding: 80px 0;
    margin-top: 30px;
}

.features-content {
    padding: 30px 0;
}

.features-content h2 {
    font-size: 32px;
    font-weight: 700;
    margin-bottom: 20px;
    color: #2c3e50;
}

.features-content p {
    font-size: 16px;
    color: #666;
    margin-bottom: 30px;
    line-height: 1.8;
}

.features-list {
    list-style: none;
    padding: 0;
    margin-bottom: 30px;
}

.features-list li {
    margin-bottom: 15px;
    font-size: 16px;
    color: #555;
}

.features-list li i {
    color: #3498db;
    margin-right: 10px;
}

.features-content .btn {
    padding: 12px 30px;
    border-radius: 30px;
    font-weight: 500;
    background-color: #3498db;
    border-color: #3498db;
    color: #fff;
    transition: all 0.3s ease;
}

.features-content .btn:hover {
    background-color: #2980b9;
    border-color: #2980b9;
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.features-image {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.features-image img {
    max-width: 100%;
    border-radius: 10px;
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
}

/* 响应式调整 */
@media (max-width: 991px) {
    .service-banner {
        height: 300px;
    }
    
    .banner-content h1 {
        font-size: 36px;
    }
    
    .banner-content p {
        font-size: 18px;
    }
    
    .section-title {
        font-size: 32px;
    }
    
    .features-content {
        margin-bottom: 30px;
    }
}

@media (max-width: 767px) {
    .service-banner {
        height: 250px;
    }
    
    .banner-content h1 {
        font-size: 30px;
    }
    
    .banner-content p {
        font-size: 16px;
    }
    
    .section-title {
        font-size: 28px;
    }
    
    .Service-container {
        padding: 15px 0;
    }
    
    .Service-item {
        padding: 0 10px;
    }
}

@media (max-width: 480px) {
    .service-banner {
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
    
    .Service-item-top {
        height: 100px;
        padding: 20px;
    }
    
    .Service-item-img {
        height: 160px;
    }
}
</style>

