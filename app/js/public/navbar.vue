<template>
    <Panel :class="$style.panel"
           title="导航栏">
        <ul :class="$style.content">
            <li v-for="item in items"
                :key="item.img">
                <router-link :to="{name:item.herf}">
                    <img :src="item.img"
                         alt="">
                    <p>{{ item.name }}</p>
                </router-link>
            </li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"

export default {
    components: {
        Panel,
    },
    data() {
        return {
            items: [{
                herf: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/8325/8/4331/3095/5bda5c89E1be47c14/47b6a296683a12a5.png?width=90&height=90",
                name: "首页",
            }, {
                herf: "money",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/1890/15/14183/1269/5bda5c97E34734b01/241a0f5b17fd3e51.png?width=60&height=60",
                name: "赚钱",
            },
            {
                herf: "borrow",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/5291/40/14133/594/5bda5ca3E92d0e800/09ac81fa5a5c96ef.png?width=60&height=60",
                name: "借钱",
            },
            {
                herf: "save",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/3358/38/14064/816/5bda5cabEcb7eca8b/9bb064f1cda7ceba.png?width=60&height=60",
                name: "省钱",
            },
            {
                herf: "mine",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/7491/15/4277/926/5bda5cb9E421a0e60/89ee14ce9daf4aab.png?width=60&height=60",
                name: "我的",
            }],
        }
    },
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  margin-top: 0 !important;
  margin-bottom: 0 !important;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  height: 100px;
  z-index: 1000;
  > h4 {
    display: none;
  }
  .content {
    @include flex(row);
    justify-content: space-around;
    li {
      text-align: center;
      a {
        text-decoration: none;
      }
      img {
        height: 44px;
        width: 44px;
        display: inline-block;
        margin: 12px auto 6px;
      }
      p {
        font-size: 22px;
        color: #656565;
      }
    }
  }
}
</style>
