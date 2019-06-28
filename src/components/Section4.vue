<template>
  <div class="section">
    <div class="section4">
      <div class="container">
        <div class="box">
          <div class="title">
            <img src="../assets/link-idol/timeline/1.png" alt="">
            <h1>链接偶像企划诞生</h1>
          </div>
          <div class="bg-time">2018.2</div>
        </div>
        <div class="box">
          <div class="title">
            <h1>
              链接偶像最初6个角色诞生：<br>
              比特币、EOS、区块链、狗狗币、<br>
              sari(吉祥物)、质数币
            </h1>
            <img src="../assets/link-idol/timeline/2.png" alt="">
          </div>
          <div class="bg-time">2018.4</div>
        </div>
        <div class="box">
          <div class="title">
            <img src="../assets/link-idol/timeline/3.png" alt="">
            <h1>在CP22上发布初版设定集《link-idol》</h1>
          </div>
          <div class="bg-time">2018.5</div>
        </div>
        <div class="box">
          <div class="title">
            <h1>在CP23上发布第二版设定集《NODE》</h1>
            <img src="../assets/link-idol/timeline/4.png" alt="">
          </div>
          <div class="bg-time">2018.12</div>
        </div>
        <div class="box">
          <div class="title">
            <img src="../assets/link-idol/timeline/5.png" alt="">
            <h1>在CP24上与智能签名合作发布数字版</h1>
          </div>
          <div class="bg-time">2019.5</div>
        </div>
        <div class="box">
          <div class="title">
            <h1>参加日本技术书典</h1>
            <img src="../assets/link-idol/timeline/6.png" alt="">
          </div>
          <div class="bg-time">2019.9</div>
        </div>
      </div>
      <div class="center-line"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Section4'
}
</script>

<style lang="less" scoped>
.section4 {
  margin-left: 200px;
  box-sizing: border-box;
  height: 100%;
  background-image: url("../assets/link-idol/bg-timeline.png");
  background-position: 0% 50%;
  background-size: cover;
  background-repeat: repeat-x;
  position: relative;
  padding-bottom: 20px;
}
.container {
  overflow-x: scroll;
  height: 100%;
  white-space: nowrap;
  display: flex;
  align-items: center;
  flex-wrap: nowrap;
}
.box {
  width: 80%;
  flex-shrink:0;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  .title {
    z-index: 10;
    text-align: center;
    img {
      height: 140px;
    }
    h1 {
      height: 100px;
    }
  }
  .bg-time {
    z-index: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: #E6F9F7;
    font-size: 200px;
    font-style:italic;
    font-weight: 700;
  }
}
.center-line {
  position: absolute;
  background: #B6F5EC;
  top: 50%;
  left: 0;
  width: 100%;
  height: 1px;
  z-index: 0;
}
</style>
<style lang="less">
  /* 设置滚动条的样式 */
  ::-webkit-scrollbar {
    width:10px;
  }
  /* 滚动槽 */
  ::-webkit-scrollbar-track {
    background: rgba(0,0,0,0.1);
    -webkit-box-shadow:inset006pxrgba(0,0,0,0.7);
    border-radius:10px;
  }
  /* 滚动条滑块 */
  ::-webkit-scrollbar-thumb {
    border-radius:10px;
    background: #96EFE3;
    -webkit-box-shadow:inset006pxrgba(0,0,0,0.5);
  }
  ::-webkit-scrollbar-thumb:window-inactive {
    background: #96EFE3;
  }
</style>
