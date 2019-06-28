<template>
  <div class="carousel">
    <button class="arrow" @click="prev" :disabled="imgIdx <= 0">
      <img src="../assets/link-idol/left.png" alt="">
    </button>
    <div :class="type === 0 ? 'carousel-window' : 'carousel-window2'" :style="`width: ${d * displayWidth}px`">
      <div :class="type === 0 ? 'carousel-container' : 'carousel-container2'" :style="containerStyle">
        <div v-for="(item, i) in avatar" :class="['carousel-item', {'active': imgIdx === i}]" :key="i" :style="`transform: translateX(${i * imgWidth}px) scale(1);`" @click="move(i)">
          <img :src="item.src" alt="">
        </div>
      </div>
    </div>
    <button class="arrow" @click="next" :disabled="imgIdx >= avatar.length - 1">
      <img src="../assets/link-idol/right.png" alt="">
    </button>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  props: { 
    avatar: {
      type: Array,
      default: () => []
    },
    type: {
      type: Number,
      default: 0
    },
    imgWidth: {
      type: Number,
      default: 100
    },
    displayWidth: {
      type: Number,
      default: 100
    }
  },
  data () {
    return {
      imgIdx: 0, // 第几张图片
      displayIdx: 0, // 显示位置
      d: 5, // 显示几张图片
    }
  },
  computed: {
    containerStyle() {  //这里用了计算属性，用transform来移动整个图片列表
      return {
        transform:`translate3d(-${this.displayIdx * this.imgWidth}px, 0, 0)`
      }
    }
  },
  methods: {
    prev() {
      let { imgIdx, displayIdx, d, avatar } = this;
      const l = avatar.length;
      if (displayIdx > 0 && imgIdx === displayIdx) this.displayIdx --;
      if (imgIdx > 0) { 
        this.imgIdx --;
        this.$emit('prev', this.imgIdx);
      }
    },
    next() {
      let { imgIdx, displayIdx, d, avatar } = this;
      const l = avatar.length;
      if (displayIdx < l-d && imgIdx === d + displayIdx - 1) this.displayIdx ++;
      if (imgIdx < l - 1) {
        this.imgIdx ++;
        this.$emit('next', this.imgIdx);
      }
    },
    move(i) {
      this.imgIdx = i;
      this.$emit('move', i)
    }
  }
}
</script>

<!--比特币#FAE78A  以太币#D3F196   以太经典#94EFB8    EOS#F6CAD5    质数币#F6CAD5     狗狗币#F5DD8E-->
<style lang="less" scoped>
.arrow {
  border: none;
  outline: none;
  padding: 0;
  margin: 0 10px;
  cursor: pointer;
  background-color: transparent;
  img {
    width: 20px;
  }
}
.arrow:disabled {
  opacity: 0.4;
  cursor: not-allowed;
}
.carousel {
  overflow-x: hidden;
  position: relative;
  display: flex;
  align-items: center;
}
.carousel-window {
  overflow: hidden;
}
.carousel-window2 {
  overflow: hidden;
  transform: skewX(-28deg);
  display: inline-block;
}
.carousel-container {
  text-align: center;
  height: 120px;
  transition: all 100ms ease-in;
  width: auto;
  position: relative;
  .carousel-item {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100px;
      height: 100px;
      display: inline-block;
      overflow: hidden;
      z-index: 0;
      cursor: pointer;
      img {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        border: 6px solid #BBFAF9;
        opacity: 0.5;
      }
      &:hover:not(.active) {
        img {
          border-color: #BBFAF9;
          opacity: 1;
        }
      }
  }
  .active {
    img {
      border-color: #BBFAF9;
      opacity: 1;
    }
  }
}
.carousel-container2 {
  text-align: center;
  height: 88px;
  transition: all 100ms ease-in;
  width: auto;
  position: relative;
  .carousel-item {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 179px;
      height: 88px;
      display: inline-block;
      overflow: hidden;
      z-index: 0;
      cursor: pointer;
      .image-container {
        // display: inline-block;
        // transform: skewX(-45deg);
      }
      img {
        width: 203px;
        height: 76px;
        // border: 6px solid #f0f0f0;
        opacity: 0.6;
        transform: skewX(28deg) scale(1);
      }
      &:hover:not(.active) {
        img {
          // border-color: #BBFAF9;
          opacity: 1;
        }
      }
  }
  .active {
    img {
      // border-color: #BBFAF9;
      opacity: 1;
    }
  }
}
</style>
