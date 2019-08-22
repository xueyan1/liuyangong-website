<template>
    <Panel :class="$style.panel"
           title="ETC免费领">
        <section :class="$style.content">
            <router-link :to="{name:'home'}">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/41135/30/10013/75628/5d381d88Ecd1752b4/67c54ef90ae21274.png?width=750&height=200"
                     alt="">
            </router-link>
        </section>
    </Panel>
</template>
<script>
import Panel from "../core/panel.vue"

export default {
    components: {
        Panel,
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  >h4 {
    display: none
  }
  .content {
    padding-bottom: 40px;
    img {
      display: block;
      width: 100%;
    }
  }
}
</style>
