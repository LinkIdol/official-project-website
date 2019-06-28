<template>
  <div id="app">
    <full-page ref="fullpage" :options="options" id="fullpage">
      <Section1 />
      <Section2 />
      <Section3 />
      <Section4 />
      <Section5 />
    </full-page>
    <div :class="['sideNav', { 'fadeInLeft': active !== 0 }, {'section1': active === 0}]">
      <ul>
        <li v-for="(item, i) in menu" :key="i" @click="jumpTo(i)" :class="{'active': active === i}">
          <div>
            <div class="yellow">{{topSub[i]}}</div>
            {{item}}
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Section1 from '@/components/Section1'
import Section2 from '@/components/Section2'
import Section3 from '@/components/Section3'
import Section4 from '@/components/Section4'
import Section5 from '@/components/Section5'
export default {
  name: 'app',
  components: {
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
  },
  data() {
    return {
      options: {
        menu: '#menu',
        anchors: ['page1', 'page2', 'page3', 'page4', 'page5'],
        sectionsColor: ['#ffffff', '#ffffff', '#ffffff'],
        onLeave: this.onLeave,
      },
      active: 0,
      menu: ['开篇', '币娘展示', '插画节选', '时间轴', '社团简介'],
      topSub: ['Start', 'Showcase', 'Illusrations', 'Timeline', 'Circle']
    }
  },
  mounted() {
    document.querySelector('#app').setAttribute("class", 'page-active');
  },
  methods: {
    onLeave(origin, destination, direction) {
      this.active = destination.index;
    },
    jumpTo(i) {
      this.active = i;
      fullpage_api.moveTo(i+1);
    }
  }
}
</script>

<style lang="less">
@import './animate.less';
#app {
  font-family: "PingFang SC", "Helvetica Neue", Helvetica, "Nimbus Sans L", Arial, 
  "Liberation Sans", "Hiragino Sans GB", "Source Han Sans CN Normal", 
  "Microsoft YaHei", "Wenquanyi Micro Hei", "WenQuanYi Zen Hei", 
  "ST Heiti", SimHei, "WenQuanYi Zen Hei Sharp", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-width: 1200px;
}
html, body {
  margin: 0;
}
.page-active {
  .sideNav {
    .animated();
    animation-delay: .2s;
  }
}
.section1 {
  animation: 'fadeOutLeft';
  animation-delay: .2s;
}
.sideNav {
  position: fixed;
  top: 30%;
  left: 0;
  color: #333333;
  font-size: 20px;
  font-weight: 600;
  transition: all 100ms ease-in;
  ul {
    padding-left: 25px;
  }
  li {
    display: flex;
    align-items: center;
    list-style-type: none;
    line-height: 28px;
    margin-bottom: 20px;
    user-select: none;
    cursor: pointer;
    transition: all 100ms ease-in;
    &:before {
      content: "";
      width: 10px;
      height: 10px;
      display: inline-block;
      position: relative;
      background: #B2B2B2;
      border-radius: 50%;
      margin-right: 15px;
    }
    &:last-child {
      margin-bottom: 0;
    }
    &:hover:not(.active) {
      color: #000000;
      transform: translate(15px, 0px) scale(1.3);
      transition: all 100ms ease-in;
      &::before {
        background: #F7B500;
      }
    }
    .yellow {
      display: none;
    }
  }
  .active {
    color: #000000;
    transform: translate(15px, 0px) scale(1.3);
    transition: all 100ms ease-in;
    &::before {
      background: #F7B500;
    }
    .yellow {
      display: block;
      color: #FFD553;
      font-size: 13px;
      line-height: 13px;
    }
    /*>div:first-child {
      &::before {
        content: 'Showcase';
        display: block;
        color: #FFD553;
        font-size: 13px;
        line-height: 13px;
      }
    }*/
  }
}
</style>
