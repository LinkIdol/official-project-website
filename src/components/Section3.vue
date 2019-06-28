<template>
  <div class="section">
    <div class="section3">
      <div class="album">
        <img :src="album[i]" alt="">
      </div>
      <div class="detail">
        <h1>{{text[i].title}}</h1>
        <img :src="thumbnail[i]" alt="" class="thumbnail">
        <h2>{{text[i].subtitle}}</h2>
        <p class="content" v-html="text[i].content"></p>
      </div>
      <carousel @prev="prev" @next="next" class="carousel" @move="move" :avatar="avatar" :type="2"  :imgWidth="180" :displayWidth="183.8"/>
    </div>
  </div>
</template>

<script>
import carousel from './carousel';
//avatar
import avatar1 from '../assets/link-idol/album-avatar/1.png';
import avatar2 from '../assets/link-idol/album-avatar/2.png';
import avatar3 from '../assets/link-idol/album-avatar/3.png';
import avatar4 from '../assets/link-idol/album-avatar/4.png';
import avatar5 from '../assets/link-idol/album-avatar/5.png';
import avatar6 from '../assets/link-idol/album-avatar/6.png';
import avatar7 from '../assets/link-idol/album-avatar/7.png';
import avatar8 from '../assets/link-idol/album-avatar/8.png';
// thumbnail
import thumbnail1 from '../assets/link-idol/album-thumbnail/1.png';
import thumbnail2 from '../assets/link-idol/album-thumbnail/2.png';
import thumbnail3 from '../assets/link-idol/album-thumbnail/3.png';
import thumbnail4 from '../assets/link-idol/album-thumbnail/4.png';
import thumbnail5 from '../assets/link-idol/album-thumbnail/5.png';
import thumbnail6 from '../assets/link-idol/album-thumbnail/6.png';
import thumbnail7 from '../assets/link-idol/album-thumbnail/7.png';
import thumbnail8 from '../assets/link-idol/album-thumbnail/8.png';
// album
import album1 from '../assets/link-idol/album/1.png';
import album2 from '../assets/link-idol/album/2.png';
import album3 from '../assets/link-idol/album/3.png';
import album4 from '../assets/link-idol/album/4.png';
import album5 from '../assets/link-idol/album/5.png';
import album6 from '../assets/link-idol/album/6.png';
import album7 from '../assets/link-idol/album/7.png';
import album8 from '../assets/link-idol/album/8.png';

export default {
  name: 'Section3',
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
        {src: avatar8},
      ],
      thumbnail: [thumbnail1, thumbnail2, thumbnail3, thumbnail4, thumbnail5, thumbnail6, thumbnail7, thumbnail8],
      album: [album1, album2, album3, album4, album5, album6, album7, album8],
      text: [{
          title: `平时的比特币是怎样的？`,
          subtitle: `闪亮明星`,
          content: `加密货币的代表，比特币小姐。<br>
          她无时无刻不在全力以赴。<br>
          加密货币的基础就是人与货币之间的信任关系。<br>
          为了让更多的人信任自己，为了让更多的人了解自己。<br>
          比特币今天也在不懈努力。<br>
          奋斗的少女永远是闪闪发亮的明星。<br>
          Fight on！比特币！<br>`,
        },{
          title: `后生可畏`,
          subtitle: `柚子币的梦境`,
          content: `“呼呼呼……总有一天我会变成人人都敬仰的最强加密货币……” <br>“哇……柚子币小姐真是目标远大呢……” <br>在偶然的机会下，窥探到后辈梦境的比特币。 <br>柚子币那过于纯粹的野心令她不禁感到十分耀眼。 <br>曾几何时，比特币自己也曾充满雄心壮志。 <br>不过在严酷的现实面前也只能学着妥协。 <br>但现在是不是应该重新回顾一下初心呢？`,
        },{
          title: `非同寻常的一次硬分叉`,
          subtitle: `以太币与经典以太币`,
          content: `凝望彼此，如同镜中倒影。 <br>但我们却并非相同的存在。 <br>事实恰好相反， <br>我们踏上的是截然不同的两条道路。 <br>在那命运的一天， <br>由于人类理念的冲突，<br> 少女被一分为二。`,
        },{
          title: `加密猫狂潮来袭`,
          subtitle: `风靡一时的加密猫`,
          content: `凝望彼此，如同镜中倒影。 <br>但我们却并非相同的存在。 <br>事实恰好相反， <br>我们踏上的是截然不同的两条道路。 <br>在那命运的一天， <br>由于人类理念的冲突，<br> 少女被一分为二。`,
        },{
          title: `人前人后`,
          subtitle: `精英路线 对 大众路线`,
          content: `“咖啡在手，天下我有。 <br>成功的business lady就应该随时保持优雅淡定。<br>”这句话真是朗朗上口^.^ <br>今天的以太币依然是一副潇洒的模样，<br>从容不迫地处理着商业事务。<br> 应该说不愧是加密货币界的Super star？ <br>话虽如此，若是遇上过于嚣张的后辈，<br> 一场不那么优雅的大战可能就会一触即发。`,
        },{
          title: `光彩的背后`,
          subtitle: `占据上风的柚子币`,
          content: `“哈啊……又输给了后辈，我真是个useless的废物……” <br>成功的背后往往有着巨大的压力。 <br>面对业绩蒸蒸日上的后辈柚子币（EOS），<br> 以太币前辈的压力之大可想而知。 <br>今天也输给了她！不甘心！ <br>回到房间之后的以太币开始在角落里坐地画圈圈。 <br>谁都好，快去安抚少女受伤的心灵！`,
        },{
          title: `Every Day Be Happy！`,
          subtitle: `网络模因`,
          content: `加密货币之中的开心果狗狗币。 <br>与其他人不同，一切难懂的事情都与她无关。 <br>尽情享受每一天的快乐才是她的宗旨。 <br>“汪！汪！汪！” <br>“嗯嗯！Doge今天也是元气满满！Let’go 散步！”`,
        },{
          title: `加勒比岛国参加冬奥会`,
          subtitle: `比基尼与雪橇`,
          content: `在狗狗币的支援之下，牙买加雪橇队得以参加2014年的索契冬奥会。 <br>Doge自己也偷偷去雪上过了把瘾。 <br>作为加勒比海的岛国，牙买加出身的雪橇队的实力可想而知， <br>他们只得到了第30名的成绩。 <br>不过这又有什么关系？体育比赛就是重在参与。 <br>只要Happy，就一切Alright！”`,
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
.section3 {
  box-sizing: border-box;
  height: 100%;
  background-image: url("../assets/link-idol/bg-album.png");
  background-size: contain;
  display: flex;
  position: relative;
  padding: 50px 0 140px 230px;
}
.detail {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
  position: relative;
  h1 {
    margin-top: 0;
  }
  h2 {
    margin-bottom: 0;
  }
  .thumbnail {
    height: 120px;
  }
  .content {
    text-align: center;
    line-height: 40px;
    max-height: calc( 100% - 240px );
    overflow: auto;
  }
}
.album {
  width: auto;
  height: 100%;
  position: relative;
  img {
    height: 100%;
    max-height: 700px;
  }
}
.carousel {
  position: absolute;
  bottom: 20px;
  right: 20px;
}
</style>
