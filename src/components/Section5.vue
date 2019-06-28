<template>
  <div class="section">
    <div class="section5">
      <div class="album">
        <img src="../assets/link-idol/group/blockchain.png" alt="">
      </div>
      <div class="detail">
        <h1>社团名称：Link-Idol | 链接偶像</h1>
        <div class="content">
          <p>链接偶像社团建立与2018年4月，首次亮相在魔都CP22。</p>
          <p>社团成员中超过80%的部员是来自于科技公司的大佬，因为我们都相信区块链技术会成为人类未来的生活组成部分。然而区块链的高门槛属性在当前严重阻碍了大众去了解，因此新的世界需要由我们的创作来开启！</p>
          <p>我们秉承着利用二次元文化普及区块链知识的信念开始创作了一系列的内容，也就是您现在看到的设定集、插画、表情包、台历。在我们的作品中无处不在的 MEME 和小知识正是我们想要传达的知识。</p>
          <p>我们欢迎任何形式的二次创作 ！你们充满想象力的再创作，将是助推区块链行业跨入二次元领域的强大动力 ！ </p>
          <p>我们从同人出身，自然也明白同人对于官方的重要意义。就冲着这么可爱的角色，画师们还没有开始冲动吗！</p>
        </div>
        <p>
          <a href="https://pan.baidu.com/s/12bQ5lDrl2XstXuyzvpP-Iw" target="_blank">立即下载 LinkIdol 表情包</a> | 提取码gfxf
        </p>
        <div class="social">
          <div class="wechat">
            <div class="wechat-logo">
              <img src="../assets/link-idol/group/wechat.png" alt="">
            </div>
            <div>
              <p class="socialName">
                <img src="../assets/link-idol/group/weixin-icon.png" alt="wechat">
                微信公众号
              </p>
              <p>「链接偶像」</p>
            </div>
          </div>
          <div class="weibo">
            <img src="../assets/link-idol/group/weibo.png" alt="">
            <div>
              <p class="socialName">
                <img src="../assets/link-idol/group/weibo-icon.png" alt="wechat">
                <span>官方微博</span>
              </p>
              <p>「链接偶像」</p>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Section5'
}
</script>

<style lang="less" scoped>
p {
  line-height: 30px;
}
.section5 {
  box-sizing: border-box;
  height: 100%;
  background-image: url("../assets/link-idol/bg-group.png");
  background-size: contain;
  padding: 50px 0 50px 230px;
  display: flex;
}
.album {
  width: auto;
  height: 100%;
  position: relative;
  img {
    height: 100%;
  }
}
.content {
  overflow: auto;
  max-height: calc( 100% - 300px );
}
.social {
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 100%;
}
.socialName {
  display: flex;
  align-items: center;
  justify-content: center;
  img {
    margin-right: 5px;
  }
}
.detail {
  padding: 0 50px;
  max-width: 50%;
}
.wechat, .weibo {
  text-align: center;
  p {
    margin: 0;
    line-height: 30px;
  }
}
.wechat-logo {
  height: 152px;
  display: flex;
  align-items: center;
  justify-content: center;
}
h1 {
  margin-top: 0;
}
</style>
