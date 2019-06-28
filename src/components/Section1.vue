<template>
  <div class="section">
    <div class="home">
      <div class="idols fadeInRight"></div>
      <img class="logo fadeInDown" src="../assets/link-idol/logo.png" alt="">
      <img class="title fadeInUp" src="../assets/link-idol/home-title.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Section1'
}
</script>

<style lang="less" scoped>
.page-active {
  .idols {
    .animated();
    animation-delay: 1s;
    animation-duration: 3s;
  }
  .logo {
    .animated();
    animation-delay: 1s;
    animation-duration: 3s;
  }
  .title {
    .animated();
    animation-delay: 1s;
    animation-duration: 3s;
  }
}
.home {
  height: 100%;
  background-image: url("../assets/link-idol/bg-home.png");
  background-size: contain;
  position: relative;
  .logo {
    position: absolute;
    width: 40%;
    left: 20px;
    top: 0;
  }
  .title {
    position: absolute;
    width: 20%;
    left: 50px;
    bottom: 50px;
  }

  .idols {
    position: absolute;
    background-image: url("../assets/link-idol/人物-手机版.png");
    background-position: top left;
    background-size: cover;
    right: 0;
    height: 100%;
    width: 60%;
  }
}

</style>
