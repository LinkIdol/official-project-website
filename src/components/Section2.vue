<template>
  <div class="section">
    <div class="section2" :style="`background-image: url(${bg[i]});`">
      <div class="left-section">
        <img :src="title[i]" alt="blockchain" class="title-img">
        <div class="info" v-html="text[i].info">
        </div>
        <div class="content" v-html="text[i].content">
        </div>
        <carousel @prev="prev" @next="next" class="carousel" @move="move" :avatar="avatar"/>
      </div>
      <div class="right-section">
        <img :src="p[i]" alt="blockchain">
      </div>
      <div class="desc" v-html="text[i].desc">
      </div>
    </div>
  </div>
</template>

<script>
import carousel from './carousel';
// avatar
import avatar1 from '../assets/link-idol/idol/avatar/1.png';
import avatar2 from '../assets/link-idol/idol/avatar/2.png';
import avatar3 from '../assets/link-idol/idol/avatar/3.png';
import avatar4 from '../assets/link-idol/idol/avatar/4.png';
import avatar5 from '../assets/link-idol/idol/avatar/5.png';
import avatar6 from '../assets/link-idol/idol/avatar/6.png';
import avatar7 from '../assets/link-idol/idol/avatar/7.png';
// title
import title1 from '../assets/link-idol/idol/title/1.png';
import title2 from '../assets/link-idol/idol/title/2.png';
import title3 from '../assets/link-idol/idol/title/3.png';
import title4 from '../assets/link-idol/idol/title/4.png';
import title5 from '../assets/link-idol/idol/title/5.png';
import title6 from '../assets/link-idol/idol/title/6.png';
import title7 from '../assets/link-idol/idol/title/7.png';
//p
import p1 from '../assets/link-idol/idol/p/1.png';
import p2 from '../assets/link-idol/idol/p/2.png';
import p3 from '../assets/link-idol/idol/p/3.png';
import p4 from '../assets/link-idol/idol/p/4.png';
import p5 from '../assets/link-idol/idol/p/5.png';
import p6 from '../assets/link-idol/idol/p/6.png';
import p7 from '../assets/link-idol/idol/p/7.png';
//bg
import bg1 from '../assets/link-idol/idol/bg/1.png';
import bg2 from '../assets/link-idol/idol/bg/2.png';
import bg3 from '../assets/link-idol/idol/bg/3.png';
import bg4 from '../assets/link-idol/idol/bg/4.png';
import bg5 from '../assets/link-idol/idol/bg/5.png';
import bg6 from '../assets/link-idol/idol/bg/6.png';
import bg7 from '../assets/link-idol/idol/bg/7.png';
export default {
  name: 'Section2',
  components: {
    carousel
  },
  data() {
    return {
      avatar: [
        {src: avatar1},
        {src: avatar2},
        {src: avatar3},
        {src: avatar4},
        {src: avatar5},
        {src: avatar6},
        {src: avatar7},
      ],
      title: [title1, title2, title3, title4, title5, title6, title7],
      p: [p1, p2, p3, p4, p5, p6, p7],
      bg: [bg1, bg2, bg3, bg4, bg5, bg6, bg7],
      text: [
        {
          info: `<p>诞生时间：2009年1月9日</p>
          <p>创造者：中本聪（Satoshi Nakamoto)</p>
          <p>官方网站：blockchain.com</p>`,
          content: `<p>
            区块链大人是加密货币得以诞生的基础，她是我们所有人的母亲，也是创造了这个世界的女神一般的存在。或者应该这么说——区块链大人即是我们生活的这个世界本身。正是因为有了区块链大人那一即是全，全即是一，无法被改变和删除的特性作为基础，像我这样的虚拟货币才能够获得存在的意义。
          </p>
          <p>
            区块链大人也是一样。她既是命运女神，也是被纺织出来的布匹本身。是的，区块链大人的真身，乃是所有链接到这一网络上的节点的记录的集合体。从这个意义上来说，她更接近一种概念而非实体，因此区块链大人的形象也是千变万化的。现在你们看到的是作为我们加密货币的母亲的形象，她的许多条手臂无时无刻不在纺织着新的记录，而那也是我们虚拟货币得以存在与成长的根基所在。
          </p>`,
          desc: `<p>「我乃区块链…… </p>
        <p>人类，欢迎来到我的国度。」</p>`
        },
        {
          info: `<p>始发时间：2009年1月9日</p>
<p>创造者：中本聪（Satoshi Nakamoto)</p>
<p>官方网站：bitcoin.com</p>`,
          content: `<p>
初次见面，我的名字是比特币。在所有诞生于区块链基础之上的加密货币之中，我是第一个获得了实体的存在。从这个意义上来说，我应该算是这个群体的代表吧。
</p>
<p>
不过也确实如此，说是长女，我只不过是诞生的时间比较早而已，并没有成熟到能够自称大家姐姐的程度。比特币这个概念最早被提出是在2008年的白皮书中，但正式诞生则是在2009年。到现在也还没满十岁呢。而在2010年，有一位程序员用一万比特币向网友买了两个披萨，虽然只是一件小事，但却第一次证明了我拥有真正的购买力。 如今的我已经比起当年成长了很多。但这还是不够…… 我更希望的是能在未来和其他货币同台竞技。为此我需要的是自由发展的空间。不过目前看来，这个梦想距离实现还很遥远…… 到那个时候也请你多多指教咯！。
</p>`,
          desc: `<p>「你好，人类先生！我是比特币，是加密货币的代表哦！</p>
<p>不过这话你可别让其他人听到，她们会生气的。」</p>`
        },
        {
          info: `<p>始发时间：2015年7月30日</p>
<p>创造者：维塔利克·布特林、加文·伍德、约瑟夫·鲁宾</p>
<p>官方网站：ethereum.org</p>`,
          content: `<p>Hello！大家好！人家的名字是以太币，今年刚满四岁，是加密货币之中的超级明星！ </p>
<p>嗯嗯？你说比特币前辈？讨厌啦，人家当然知道业界最大腕的明星是比特币前辈啦！我对比特币前辈那可是超~~~~~~尊敬的说。毕竟她是我们所有人的大前辈嘛！ </p>
<p>不过呢，人家的理念与比特币前辈还是有那么一点不一样的。你看，比特币前辈的区块链只负责记录账本，做不了其它的事情不是吗？人家觉得那样超~~~~~~无聊的，好不容易建立起了节点网络，当然要用它来做一些更酷的事情才好啊！所以人家就想出了一个叫“世界计算机”的很厉害的计划，不管是谁只要付给我手续费，就可以用人家的世界计算机来做他们想要做的事情。这样我能赚到钱，他们也能实现自己的梦想，完全是双赢的完美状况嘛！</p>`,
          desc: `<p>「Hi~~~~~！人家是大家的好朋友，以太币唷！ </p>
<p>快来加入世界计算机计划吧！Join me！Be free！」</p>		`
        },
        {
          info: `<p>始发时间：2015年7月30日</p>
<p>创造者：维塔利克·布特林、加文·伍德、约瑟夫·鲁宾</p>
<p>官方网站：ethereumclassic.org</p>`,
          content: `<p>你好……我的名字是以太币。不……现在应该叫“以太经典”才对…… 你应该已经遇见过自称是以太币的那位加密货币了吧？她是另一个我，是从我体内诞生出来的分身一般的存在。</p>
<p>什么，你说外表看上去我才像是妹妹？呵呵……你说话还真直白呢。确实是这样，现在的以太币比我这个原型要来得更强大，更成熟得多。我们的分裂来源于2016年的一次事件，在那起安全事故之中，黑客盗走了大量的以太币。所以以太币的用户决定要让我分叉，大多数人都同意改写代码以修复安全漏洞，但仍有少部分人坚持维持原代码不变，因为对他们来说代码就是法律（Code Is Law）。 </p>
<p>所以我们两人就这样诞生了，一个是新生的以太币，一个是我，以太经典。我的存在代表着一种信念，那是成为我们基础的区块链大人所代表的理念——即一切记录都是不可篡改的。我为这样的自己感到自豪。 </p>`,
          desc: `<p>「我曾经的名字是以太币， </p>
<p>现在则被称为以太经典，请不要搞混了哦？」</p>`
        },
        {
          info: `<p>始发时间：2018年1月31日</p>
<p>创造者：丹尼尔·拉里默、布兰登·布鲁默</p>
<p>官方网站：eos.io</p>`,
          content: `<p>呵呵呵，欢迎来到我的圣域。初次见面，我的名字是EOS。</p>
<p>什么？柚子币？呵呵，EOS这三个字母，要是念快了的话不就有点像是“柚子”一样吗？因此我就被取了那样的外号。</p>
<p>好了，来说说名字之外有关我的事情吧？你应该知道，我们加密货币都是为了实现某个理念而被创造出来的存在。我也不例外。我的目标是世界计算机——一个由无数节点组成的巨大的网络。所有人都可以利用它来运行自己的程序，而且不需要支付任何费用，只需要把自己所持的柚子币抵押出去就行了。</p>
<p>我所奉行的是精英主义，而且在谈论理想之前，我首先看中的是成效。由于这种做法，有一些人觉得我不像是纯粹的加密货币，倒像是一个用来吸金的产品。呵呵，我不会反驳他们什么，因为从某种程度上看，那也是事实呢。只不过，在看到我所获得的成绩之后，别人不管说什么都会像是出于嫉妒的妄言了吧？</p>`,
          desc: `<p>「呵呵，我是EOS，你也可以叫我柚子币。 </p>
<p>请多指教了，客人。」</p>`
        },
        {
          info: `<p>始发时间：2013年7月7日</p>
<p>创造者：桑尼·金</p>
<p>官方网站：primecoin.io</p>`,
          content: `<p>你，你好……初次见面，我的名字是质数币。</p>
<p>我的加密方式与其他人不同，主要是因为我生来就肩负着一个使命——计算这世上的数学难题，这也是我名字的来源。具体来说就是，把区块链上的节点的运算力利用起来，用来计算特定的数学问题，比如说——计算这世上最大的质数。</p>
<p>所以说……我最喜欢做的事情就是计算数字了。其他人都说我喜欢数字喜欢得过了头，就连聚会的时候也老是躲在角落盯着电脑屏幕。她们说这样做不好，应该与大家多交流一些……不，不过我觉得每个人都有自己的个性，不需要勉强自己去配合别人的喜好……</p>
<p>总而言之，我的性格就是这样，属于不善于与人交流的那种类型……不，不过这仅限于口头交流，在电脑上打字的话就没有问题了……如果可以的话，以后也请你尽量通过电脑与我对话。</p>`,
          desc: `<p>「你，你好……我是质数币…… </p>
<p>请问你对数学有兴趣吗？」</p>`
        },
        {
          info: `<p>始发时间：2013年12月6日</p>
<p>创造者：比利·马库斯、杰克逊·帕默</p>
<p>官方网站：dogecoin.com</p>`,
          content: `<p>Hello！Doge是Dogecoin！大家都叫Doge狗狗币！</p>
<p>那只在网上超火的眼神超搞笑的柴犬Doge你们都知道吧？Doge的原型就是它哦！</p>
<p>与原型的狗狗一样，Doge我的梦想也是带给网上的大家快乐！其他加密货币倡导的什么绝对公平啊绝对自由啊世界计算机什么的太复杂了，Doge搞不懂！Doge只知道在网上看到什么好料的话，想要打赏对方是很正常事。所以Doge就出来充当打赏用的小费啦！你看，Doge我又可爱又便宜，打赏的人Happy，受到小费的人也Happy，大家都Happy的话Doge我也会Happy，这不就是皆大欢喜吗！Doge真是带来快乐的天才！</p>
<p>怎么样，听了这么多，你应该对Doge很有了解了吧？以后在网上想要打赏别人的时候，千万不要忘了找Doge我帮忙哦！</p>`,
          desc: `<p>「Hello！人家的名字是狗狗币！大家请叫我Doge就好！</p>
<p>Doge的口号是：“Let’s be happy！”」</p>`
        }
      ],
      i: 0
    }
  },
  methods: {
    prev(i) {
      console.log('prev')
      this.i = i;
    },
    next(i) {
      console.log('next')
      this.i = i;
    },
    move(i) {
      console.log('move', i);
      this.i = i;
    }
  }
}
</script>

<style lang="less" scoped>
.left-section {
  width: 50%;
  height: 100%;
  margin-right: 100px;
  z-index: 8;
  .title-img {
    width: 250px;
  }
  .content {
    max-height: calc(100% - 300px);
    overflow: auto;
    p {
      line-height: 30px;
      font-size: 16px;
    }
  }
  .info {
    max-width: 300px;
    padding: 10px 20px;
    margin-bottom: 10px;
    background-color: #000000;
    color: #ffffff;
    background-color:rgba(0,0,0,0.6);
  }
  .carousel {
    position: absolute;
    z-index: 10;
    bottom: 0;
    left: 200px;
  }
}
.right-section {
  width: 50%;
  height: 100%;
  z-index: 2;
  box-sizing: border-box;
  img {
    width: auto;
    height: 100%
  }
}
.desc {
  position: absolute;
  right: 10px;
  top: 60%;
  width: 300px;
  font-weight: 700;
  z-index: 8;
}
.section2 {
  padding: 10px 0 10px 230px;
  box-sizing: border-box;
  height: 100%;
  background-size: contain;
  position: relative;
  display: flex;
  align-items: flex-start;
  justify-content: space-between
}

// .bg {
//   background-image: url("../assets/link-idol/bg1.png");
//   background-repeat: repeat;
//   background-size: contain;
//   position: absolute;
//   top: 0;
//   left: 0;
//   height: 100%;
//   width: 100%;
//   z-index: 0;
// }
</style>
<style lang="less">
.desc {
  p {
    margin: 0;
    padding: 0;
  }
  p:first-child {
    text-align: left;
  }
  p:last-child {
    text-align: right;
  }
}
.section2 {
  p {
    margin: 0;
    padding: 0;
    line-height: 30px;
    font-size: 16px;
  }
}
</style>
