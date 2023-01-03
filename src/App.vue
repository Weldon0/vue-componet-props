<template>
  <div>
    <!--3、使用helloWorld组件-->
    <HelloWorld des="1" title="篮球" price="100"></HelloWorld>
    <HelloWorld des="2" title="足球" price="200"></HelloWorld>
    <HelloWorld des="3" title="羽毛球" price="20"></HelloWorld>
    <HelloWorld des="4" title="乒乓球" price="10"></HelloWorld>

  </div>
</template>

<script>

// 父子传值
// 1、父亲怎么给儿子传值
//    自定义属性
// 1、引入hello-world组件
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  // 2、注册hello-world组件
  components: {
    HelloWorld
  },
  data() {
    return {
      content: [
        {
          "id": 3,
          "title": "数据分析 P6 高薪特训营",
          "brief": "全方位构建数据分析能力，成为抢手人才",
          "image": "https://s0.lgstatic.com/i/image/M00/81/C6/CgqCHl_RmoKAcC3WAAFcRSXIfCc142.png",
          "listImage": "https://s0.lgstatic.com/i/image/M00/81/D0/CgqCHl_Rn52ABPbzAAA6ddvYgZ4432.png",
          "href": "https://edu.lagou.com/growth/sem/data_analysis.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://edu.lagou.com/growth/sem/data_analysis.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 27,
          "brightPoints": [
            "职业新风口，高薪新选择",
            "0 基础就能学，学完就能用",
            "从理论到实战，完成职业蜕变",
            "优秀学员每月大厂内推机会"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image/M00/8E/EC/CgqCHmAGQgiAfqskAAClyQVZEpw724.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image2/M01/06/CD/Cip5yGAGQg2AS-1TAAAp8M3pw70855.png"
        },
        {
          "id": 2,
          "title": "Java P7 高薪特训营",
          "brief": "对标阿里 P7 技术能力，构建架构师 9 大技能",
          "image": "https://s0.lgstatic.com/i/image/M00/81/BA/Ciqc1F_RmneAebIgAAGeG3_wpkU277.png",
          "listImage": "https://s0.lgstatic.com/i/image/M00/81/C8/CgqCHl_RmvuATMJXAABGWcE4ZDA828.png",
          "href": "https://edu.lagou.com/growth/sem/java_architect.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://edu.lagou.com/growth/sem/java_architect.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 4,
          "brightPoints": [
            "1000+ 核心技能点 精准突破",
            "9 大维度 锻造必备架构技能",
            "10+大厂项目 真学真练真应用",
            "优秀学员 可享名企定向内推"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image/M00/8D/06/CgqCHl_286aAKwHDAAYQJLOfZY0609.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image/M00/8C/FB/Ciqc1F_286mAGneAAAFuud4CpjQ879.png"
        },
        {
          "id": 7,
          "title": "大前端 P7 高薪特训营",
          "brief": "对标阿里 P7 技术能力，打造大前端核心竞争力",
          "image": "https://s0.lgstatic.com/i/image/M00/81/C6/CgqCHl_RmqqAbQFpAAF7tQGblTA479.png",
          "listImage": "https://s0.lgstatic.com/i/image/M00/81/C5/Ciqc1F_Rn7yAPG3-AABHTB3uxnc853.png",
          "href": "https://kaiwu.lagou.com/fe_enhancement.html?utm_source=App&utm_medium=%E8%AE%AD%E7%BB%83%E8%90%A5%E4%B8%93%E5%8C%BA&utm_campaign=App%E8%AE%AD%E7%BB%83%E8%90%A5%E4%B8%93%E5%8C%BA&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://kaiwu.lagou.com/fe_enhancement.html?utm_source=App&utm_medium=%E8%AE%AD%E7%BB%83%E8%90%A5%E4%B8%93%E5%8C%BA&utm_campaign=App%E8%AE%AD%E7%BB%83%E8%90%A5%E4%B8%93%E5%8C%BA&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 17,
          "brightPoints": [
            "高效系统的大前端进阶路径",
            "20+ 大厂项目实操 真学真练",
            "拉勾学员专享大厂内推机会",
            "匹配大厂私教 名企享优先入职"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image/M00/8C/FB/Ciqc1F_29BGAQqKUAAaWiAYTksA193.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image/M00/8D/06/CgqCHl_29BSANSsJAAGpphnHo7k590.png"
        },
        {
          "id": 6,
          "title": "大前端 P6 高薪特训营",
          "brief": "0 基础到高薪就业，成为企业需要的抢手人才",
          "image": "https://s0.lgstatic.com/i/image/M00/81/BB/Ciqc1F_RmqKAHmjkAAGo9gcoDFI685.png",
          "listImage": "https://s0.lgstatic.com/i/image/M00/81/C5/Ciqc1F_Rn7OAZrt-AABBowVuKlw934.png",
          "href": "https://edu.lagou.com/growth/sem/fe_essential.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://edu.lagou.com/growth/sem/fe_essential.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 38,
          "brightPoints": [
            "无门槛，0 基础轻松学习",
            "4个月获得 2-4 年前端经验",
            "90w+ 企业用人需求调研",
            "一份可以写在简历的实战项目"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image2/M01/04/DE/Cip5yF_28-CAUyDYAASY6r3fc5k042.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image2/M01/04/E0/CgpVE1_28-KAMwofAAFUoAJSwck630.png"
        },
        {
          "id": 8,
          "title": "Java P6 高薪特训营",
          "brief": "0 基础入行 Java 的绿色通道，精通核心技能",
          "image": "https://s0.lgstatic.com/i/image/M00/81/BB/Ciqc1F_RmrGAct0VAAF4gmbccIk045.png",
          "listImage": "https://s0.lgstatic.com/i/image/M00/81/C5/Ciqc1F_Rn8OACabcAABFOEKna7Q294.png",
          "href": "https://edu.lagou.com/growth/sem/java_basic.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://edu.lagou.com/growth/sem/java_basic.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 45,
          "brightPoints": [
            "V2.0 全新配置升级案例库",
            "深度实战 4 类主流名企项目",
            "前沿技术焊接完整知识脉络",
            "打通就业闭环助力大厂 Offer"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image/M00/8C/FB/Ciqc1F_29BqAPivcAARCy0f6s2s152.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image/M00/8D/06/CgqCHl_29ByAYGp5AAEuh9j2VzI062.png"
        },
        {
          "id": 9,
          "title": "测试开发实战训练营",
          "brief": "大厂测试专家带路，实力打造名企全栈技术",
          "image": "https://s0.lgstatic.com/i/image/M00/81/C6/CgqCHl_RmrqAEVQnAAFskbq9r-g694.png",
          "listImage": "https://s0.lgstatic.com/i/image/M00/81/C5/Ciqc1F_Rn8qAJVDUAAA7d3Nz45A535.png",
          "href": "https://edu.lagou.com/growth/sem/test_engineer.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://edu.lagou.com/growth/sem/test_engineer.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 6,
          "brightPoints": [
            "名企项目实战，构造完整测试体系",
            "大厂名师授课，还原名企能力模型",
            "5对1联合培养，打造专属核心技能",
            "陪伴式学习体验，学习更轻松"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image/M00/8C/FB/Ciqc1F_29CqANbTVAAX3gTVQL4Q567.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image/M00/8D/06/CgqCHl_29C6ADu3-AAFLDXej4_8454.png"
        },
        {
          "id": 25,
          "title": "商业分析 P7 高薪特训营",
          "brief": "90 天构建商业思维，提升业务大局观",
          "image": "https://s0.lgstatic.com/i/image6/M00/77/40/CioPOWImxEqAItpXAAUJjeA37SU566.png",
          "listImage": "https://s0.lgstatic.com/i/image6/M00/77/38/Cgp9HWImxJWAK2XdAADr-vVOxJY603.png",
          "href": "https://edu.lagou.com/growth/sem/business.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "h5Href": "https://edu.lagou.com/growth/sem/business.html?utm_source=app_edu_course_hub&biz_tpye=0&lgec_type=website&lgec_sign=D65F20B4C7267487F432755C0D45C500",
          "bigCourseId": 156,
          "brightPoints": [
            "10 大阶段提升业务大局观",
            "详析热门行业，洞悉新趋势",
            "深度还原一线大厂商业场景",
            "优秀学员每月大厂内推机会"
          ],
          "pcLargeImage": "https://s0.lgstatic.com/i/image6/M00/77/41/CioPOWImxGeAU8miAANef1RsM-g458.png",
          "pcLittleImage": "https://s0.lgstatic.com/i/image6/M01/77/38/Cgp9HWImxGyAaALUAAEAZRYTCMg753.png"
        }
      ]
    }
  },
}
</script>
