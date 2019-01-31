<template>
  <div class="part3">
    <div class="part3-container">
      <div class="part3-header">
        <div class="part3-title-container">
          <div class="title-bubble bubble1"></div>
          <div class="title-bubble bubble2"></div>
          <div class="title-font">我们推出了</div>
        </div>
        <div class="header-image"></div>
      </div>
      <div class="part3-body">
        <div class="project-card">
          <div class="project-card-header">
            <div class="project-card-name">「南邮本科生小程序」</div>
            <div
              class="project-detail"
            >轻量级移动端智慧校园解决方案。在不弃用高校现有各系统的情况下，对学生日常使用的各系统功能进行整合，并在手机上通过即走即用、无需下载的微信小程序的方式展现。</div>
          </div>
          <div class="project-card-body">
            <img src="https://static.airbob.org/homepage/under-graduate.png" alt>
          </div>
        </div>
        <div class="project-card">
          <div class="project-card-header">
            <div class="project-card-name">「南邮研究生小程序」</div>
            <div
              class="project-detail"
            >轻量级移动端智慧校园解决方案。以南邮研究生同学服务作为出发点，创造解决南邮研究生生活学习中存在的痛点的可能，提供定制化服务。</div>
          </div>
          <div class="project-card-body">
            <img src="https://static.airbob.org/homepage/graduate.png" alt>
          </div>
        </div>
        <div class="project-card">
          <div class="project-card-header">
            <div class="project-card-name">「寒假期末报告单」</div>
            <div
              class="project-detail"
              @click="navToWinterReport"
            >在2018年寒假一经推出就受到了大家的热烈追捧和转发，以活泼的画面和新鲜的内容吸引了大家的眼球。一度刷屏南邮师生的朋友圈。（体验账号：demo，密码：demo）</div>
          </div>
          <div class="project-card-body">
            <img src="https://static.airbob.org/homepage/annu1.png" alt>
          </div>
        </div>
        <div class="project-card">
          <div class="project-card-header">
            <div class="project-card-name">「暑假期末报告单」</div>
            <div
              class="project-detail"
              @click="navToSummerReport"
            >2018年暑假，第二张《南邮本科生期末报告单》再次推出，清新亮丽的画风再次引得南邮学子的认可，引发朋友圈刷屏。（体验账号：demo，密码：demo）</div>
          </div>
          <div class="project-card-body">
            <img src="https://static.airbob.org/homepage/annu2.png" alt>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: `Project`,
  methods: {
    navToWinterReport() {
      window.location.href = "https://qingyou.njupt.edu.cn/annual2017/";
    },
    navToSummerReport() {
      window.location.href = "https://qingyou.njupt.edu.cn/bgd2/";
    }
  }
};
</script>

<style lang="sass" scoped>
@import "../style/bubble.sass"
.z-top
  z-index: 1
.part3
  width: 100vw
  background-image: url('../assets/background/wave-line_3.svg')
  background-size: cover
  background-repeat: no-repeat
  display: flex
  justify-content: center
  background-position-y: -200px
  .part3-container
    width: 72%
    display: flex
    flex-direction: column
    align-items: center
    margin-bottom: 20px
    @media(max-width: $phone)
      width: 100%
    .part3-header
      width: 100%
      display: flex
      justify-content: space-between
      margin-bottom: 3.5rem
      align-items: center
      @media(max-width: $ipad)
        flex-direction: column
        align-items: flex-start
      @media(max-width: $phone)
        width: 72%
      .part3-title-container
        position: relative 
      .title-font
        font-weight: 600
        font-size: 2.5rem
        @media(max-width: $phone)
          font-size: 1.5rem
          margin-bottom: 0.625rem
        color: #222222
      .header-image
        width: 33.75rem
        height: 26.0625rem
        background-size: 70%
        background-position: center
        background-repeat: no-repeat
        @media(max-width: $ipad)
          margin: auto
          background-size: 60%
        @media(max-width: $phone)
          width: 17.5rem
          height: 13.125rem
        background-image: url('https://static.airbob.org/homepage/xiaochenxu_1.png')
    .part3-body
      width: 100%
      display: grid
      grid-template-columns: repeat(2, 1fr)
      margin-bottom: 3.125rem
      @media(max-width: $ipad)
        grid-template-columns: repeat(1, 1fr)
        margin-bottom: 0
        justify-items: center
        width: 100vw
      .project-card
        color: red
        width: 28.75rem
        height: 21.5625rem
        border-radius: 10px
        position: relative
        cursor: pointer
        @media(min-width: $ipad)
          margin-bottom: 2.225rem
        @media(max-width: $ipad)
          margin-bottom: 4.375rem
        @media(max-width: $phone)
          margin-bottom: 5rem
          width: 17.5rem
          height: 13.125rem
        &:hover
          z-index: 1 // 保证hover到的card在顶层
          .project-card-header
            transform: translateY(-50%)
          .project-card-body
            box-shadow: 0 -5px 10px -4px rgba(0,0,0,0.20)
            transform: scale(1.1) translateY(20%)
        .project-card-header
          border-radius: 1rem;
          width: 100%
          height: auto
          transition: all 0.3s ease-out 
          position: absolute
          top: 0
          background-color: #22b574
          color: #ffffff
          .project-card-name
            margin-left: 2.25rem
            padding-top: 1.5rem
            margin-bottom: 1rem
            @media(min-width: $phone)
              font-size: 1.5rem
          .project-detail
            text-align: justify
            padding: 1.25rem
            margin: auto
            line-height: 1.25rem
            font-size: 90%
            @media(min-width: $phone)
              font-size: 1.125rem
              line-height: 1.5rem
        .project-card-body
          width: 100%
          height: auto
          border-radius: 10px
          position: absolute
          transition: all 0.3s ease-out
          top: 3.75rem
          background-color: #fafafa
          background-size: cover
          display: flex
          justify-content: center
          align-items: center
          img
            margin: auto
            width: 100%
            height: 100%
            border-radius: 10px
</style>

