<template>
  <div class="part4">
    <div class="part-title-container">
      <div class="part-title-img-container" />
      <div class="title-bubble bubble1" />
      <div class="title-bubble bubble2" />
      <span class="title-text">我们欢迎</span>
    </div>
    <div class="part-content">
      <div class="card-container">
        <div 
          v-for="(item) in cardInfo.slice(0,2)" 
          :key="item.id" 
          class="content-card"
        >
          <div class="card-card card1" />
          <div class="card-card card2" />
          <div class="card-content">
            <div class="content-title">{{ item.title }}</div>
            <div class="content-text">{{ item.content }}</div>
          </div>
        </div>
      </div>
      <div class="card-container">
        <div 
          v-for="(item) in cardInfo.slice(2,4)" 
          :key="item.id" 
          class="content-card"
        >
          <div class="card-card card1" />
          <div class="card-card card2" />
          <div class="card-content">
            <div class="content-title">{{ item.title }}</div>
            <div class="content-text">{{ item.content }}</div>
          </div>
        </div>
      </div>
    </div>
    <img 
      class="part-image" 
      src="../assets/Illustrations/design_process_iqqg.svg"
    >
    <div class="part-content">
      <div class="card-container">
        <div 
          v-for="(item) in cardInfo.slice(4,6)" 
          :key="item.id" 
          class="content-card"
        >
          <div class="card-card card1" />
          <div class="card-card card2" />
          <div class="card-content">
            <div class="content-title">{{ item.title }}</div>
            <div class="content-text">{{ item.content }}</div>
          </div>
        </div>
      </div>
      <div class="card-container">
        <div 
          v-for="(item) in cardInfo.slice(6)" 
          :key="item.id" 
          class="content-card"
        >
          <div class="card-card card1" />
          <div class="card-card card2" />
          <div class="card-content">
            <div class="content-title">{{ item.title }}</div>
            <div class="content-text">{{ item.content }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: `Recruit`,
  data() {
    return {
      cardInfo: [
        {
          id: 1,
          title: "前端",
          content:
            "负责团队项目的前端开发，掌握HTML/CSS，基本了解Javascript，能与团队其他成员友好交流。"
        },
        {
          id: 2,
          title: "后端",
          content:
            "负责团队项目的后端开发，掌握爬虫的开发技巧，掌握至少一门后端开发语言，积极向上。"
        },
        {
          id: 3,
          title: "ios | android",
          content:
            "完成团队项目的多终端部署计划，掌握Object-C，Swift，Java中任意一门语言，有较强的创新精神。"
        },
        {
          id: 4,
          title: "测试工程师",
          content:
            "对团队的产品进行发布前的100%覆盖测试，有一定的全栈知识，能够预估产品Bug产生的原因。"
        },
        {
          id: 5,
          title: "界面设计",
          content:
            "负责web/移动端的界面设计，能与前端的童鞋友好交流，并且具有一定读文档的能力，积极分享设计经验。"
        },
        {
          id: 6,
          title: "画师",
          content:
            "负责以“肖辰旭”形象，风格为基础的绘制设计工作。完成产品 UI 的绘图部分和青柚文创系列的设计"
        },
        {
          id: 7,
          title: "运营",
          content:
            "掌握新媒体运营的相关技术，对互联网具有较强的敏感性，擅长策划宣传工作，熟练使用平面设计相关软件。"
        }
      ]
    };
  }
};
</script>


<style lang="sass" scoped>
@import "../style/bubble.sass"
.part4
  width: 100%
  display: flex
  flex-direction: column
  align-items: center
  .part-title-container
    margin: 0 auto
    width: 72%
    height: 40rem
    background-image: url('https://static.airbob.org/homepage/xiaochenxu_2.png')
    background-repeat: no-repeat
    background-position: center center
    position: relative
    margin-top: 2rem
    @media(max-width: $ipad)
      height: 30rem
      background-size: 50%
    @media(max-width: $phone)
      height: 15rem
    .title-text
      font-size: 2.5rem
      color: #222222
      font-weight: 600
      @media(max-width: $phone)
        font-size: 1.5rem
    .part-title-img-container
      
  .part-content
    width: 100%
    background-image: url('../assets/background/wave-line_4.svg')
    background-repeat: no-repeat
    background-size: 100%
    .card-container
      margin: 0 auto
      display: flex
      flex-direction: row
      flex-wrap: wrap
      justify-content: space-between
      align-items: center
      @media(min-width: $phone)
        width: 74%
      @media(max-width: $ipad)
        width: 92%
        justify-content: space-around
      .content-card
        position: relative
        height: 25rem
        width: 25rem
        display: flex
        align-items: center
        justify-content: center
        margin: 2rem
        @media(max-width: $phone)
          height: 18rem
          width: 18rem
          margin: 0 auto
        .card-card
          background: #dcfbb5
          width: 20rem
          height: 20rem
          opacity: 0.5
          position: absolute
          transition: all .2s ease .0s
          @media(max-width: $phone)
            height: 14rem
            width: 14rem
        .card1
          transform: rotate(10deg)
        .card2
          transform: rotate(-60deg)
        .card-content
          cursor: pointer
          height: 8rem
          width: 16rem
          display: flex
          justify-content: center
          align-items: center
          flex-direction: column
          text-align: justify
          @media(max-width: $phone)
            height: 5rem
            width: 10rem
          .content-title
            font-size: 1.4rem
            font-weight: 500
            color: #22b574
            z-index: 1
            @media(max-width: $phone)
              font-size: 1.2rem
          .content-text
            margin-top: 1rem
            color: #222222
            z-index: 1
            @media(max-width: $phone)
              font-size: 0.8rem
        &:hover
          .card1,.card2
            transform: rotate(0)
            transition: all .2s ease .0s
  .part-image
    width: 72%
    margin: 1.25rem 0
    @media(min-width: $ipad)
      height: 33.5625rem
      margin: 5rem 0
</style>
