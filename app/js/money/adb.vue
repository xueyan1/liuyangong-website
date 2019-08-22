<template>
    <Panel :class="$style.panel"
           title="ETC免费领">
        <section :class="$style.content">
            <router-link :to="{name:'home'}">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/37697/16/1334/187953/5cb44c65E5dbefe83/200ce71a4347aeec.png?width=750&height=200"
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
