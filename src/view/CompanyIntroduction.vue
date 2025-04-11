<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>厦门知命者文化产业有限公司</h3>
                    <p class=".text-justify">知命者，是一家以传统智慧与现代科技融合为核心的创新服务平台，汇聚了精通玄学文化、生命科学、环境科学及天文学等领域的顶尖专家与学者，致力于为个人与企业提供命运科学探究、生命状态分析、运程预测优化及人生规划指导等全方位解决方案。我们通过自主研发的智能提示系统，结合四柱八字、紫微斗数、中医养生等传统智慧与人工智能技术，帮助用户改善生命状态、调节时空环境，助力突破命运障碍，成就更加畅通美好的人生旅程。</p> 
                    <p class=".text-justify">我们的服务涵盖个人命运改进咨询、企业环境能量优化、传统文化传承合作等领域，客户遍及教育、医疗、文化产业、大健康行业及传统文化机构，并与国学研究院、生命科学研究所、环境工程机构等建立了深度合作。依托严谨的科学态度与深厚的文化底蕴，我们为每一位用户制定个性化方案，成功协助数千人优化生命轨迹，重塑人生价值。知命者始终以“利人利己”为根基，以创新科技赋能传统智慧，为中华文化的全球传播与时代焕新开辟全新道路，让命运科学惠及众生。</p>
                </div>
            </div>
        </div>
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
        var wow = new WOW();
        wow.init();
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 100px 0;
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

