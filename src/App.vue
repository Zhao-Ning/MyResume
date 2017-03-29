<template>
  <div class="content" id="app">
    <userInfo :model="userInfo"></userInfo>
    <Ability :model="userAbility"></Ability>
    <Project :model="projects"></Project>
    <Ability :model="selfAppraisal"></Ability>
    <urlItem :model="other"></urlItem>
  </div>
</template>

<script>
import userInfo from './components/userInfo'
import Ability from './components/Ability'
import Project from './components/Project'
import urlItem from './components/urlItem'

export default {
  name: 'app',
  data () {
    return {
      userInfo: {
        name: "赵宁",
        year: 24,
        sex: "女",
        position: "前端开发工程师",
        workTime: "2年工作经验",
        tel: "13716020908",
        email: "1991407206@qq.com",
        education: "本科",
        major: "计算机科学与技术"
      },
      userAbility: {
        label: "个人技能",
        data: [
           "熟练掌握 HTML、CSS、JS，了解ES6相关知识", 
           "CSS预处理器：熟练使用 stylus ，使用过postCSS", 
           "基本掌握 jQuery、Vue.js、Backbone.js，理解MVC、MVVM设计模式；",
           "熟练使用Bootstrap框架，能够快速构建前端页面",
           "熟练使用webpack，熟悉前端工程化和组件化开发思想；",
           "日常开发使用工具：Sublime, Git, SVN",
           "熟练使用Chrome开发者工具、Charles等工具辅助开发",
           "英语4级，阅读英文文档基本无障碍"
        ]
      },
      projects: {
        label: "工作经验",
        allProData: [
        {
          companyDate: {
            company: "正益移动互联科技股份有限公司",
            position: "前端开发工程师",
            address: "北京",
            date: "2015.09 - 至今"
          },
          proData: [{
                    proTitle: "正益工作",
                    startTime: "",
                    endTime: "",
                    proLink: "http://work.zyhao.com",
                    data: [
                      "该项目是企业级门户管理及移动办公得一体式企业级解决方案；",
                      "使用Zepto.js + Backbone.js + AppCan.js 构建的Hybrid App，我主要负责正益工作移动端App功能门户、IM会话、企业通讯录、考勤签到、工单任务报告、CRM等模块得功能开发及维护；",
                      "该项目门户模块源代码已被中国电建、上海卡斯柯、万科集团、福田汽车、奥凯航空等企业级用户所采用；",
                      "我在完善功能样式后，使用Vue.js重构部分项目，代码量减少20%"
                    ]
                  },{
                    proTitle: "中国核电-日常巡查",
                    startTime: "",
                    endTime: "",
                    proLink: "",
                    data: [
                      "该项目是中国核电工程有限公司管理工程隐患的Hybrid App；",
                      "主要负责日常巡查App功能门户、隐患排查、隐患整改模块的功能开发及维护；",
                      "使用Zepto.js + Vue.js 实现数据绑定以及组件化开发，使用AppCan.js调用原生插件完成语音识别、拍照选择手机图片等功能，编写 xml，ejs文件完成门户卡片动态配置、快捷入口功能"
                    ]
                  },{
                    proTitle: "方正证券-重点事项跟踪",
                    startTime: "",
                    endTime: "",
                    proLink: "",
                    data: [
                      "该项目是方正证券内部员工在跟踪管理重点事项的微信端平台;",
                      "负责全部前端页面的开发，包括事项管理、事项提醒、企业通讯录模块前端页面及功能的开发，并完成前后端接口的联调对接工作;",
                      "使用HTML、CSS实现静态页面，根据微信开发者文档完成图片的预览、上传、删除，使用swiper.js完成页面滑动切换效果，使用jQuery操作DOM和进行网络请求"
                    ]
                  },{
                    proTitle: "中国保险万事通",
                    startTime: "",
                    endTime: "",
                    proLink: "",
                    data: [
                      "该项目主要为中国保险消费者提供产品咨询、理财咨询、理赔咨询、投诉咨询等在线服务；",
                      "该项目两部分组成：针对消费者的Hybrid App, 以及 PC 后台管理网站",
                      "我主要负责该项目的后台管理网站，包括公司管理、客服管理、产品管理、个人中心模块的功能开发;",
                      "使用HTML、CSS、jQuery 完成页面功能，配合后端人员数据联调，并及时解决bug支持产品上线"
                    ]
                  }]          
                }
              ]
  
      },
      selfAppraisal: {
        label: "自我评价",
        data: [
          "对待工作认真负责，能够顺畅的和同事沟通",
          "对后端技术和数据库有一定了解，独立开发过应用",
          "按时保质完成分配的任务，具有单独解决bug的能力",
          "具有学习欲望和一定的自学能力"
        ]
      },
      other: {
        label: "其他",
        data: [
          {
            label: "GIT地址：",
            url: "https://github.com/zhaoning98"
          },
          {
            label: "在线简历：",
            url: "https://zhaoning98.github.io/preview/"
          }
        ]
      }
    };
  },
  components: {
    userInfo,
    Ability,
    Project,
    urlItem
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .content 
    width: 80%
    padding: 50px 0
    margin: 0 auto
</style>
