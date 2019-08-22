<template>
    <Panel :class="$style.panel"
           title="轮播图">
        <section :class="$style.content">
            <slider :items="items"
                    :cname="$style.slider" />
        </section>

    </Panel>
</template>

<script type="text/ecmascript-6">
import Slider from "../core/slider.vue"
import Panel from "../core/panel.vue"

export default {
    components: {
        Slider,
        Panel,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t1/35731/27/14378/124844/5d400a99E08530579/cba4b33a090f8ed2.png?width=750&height=400",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t1/44275/12/10265/25627/5d3a7326E25751e7f/a78bbf67ef1c9461.jpg?width=750&height=400",
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t1/56819/3/5732/50247/5d36d04dEee287aaf/4ffcd8155025e08b.jpg?width=750&height=400",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  >h4{
    display: none
  }
  .content{
    .slider{
      margin-top:120px;
      img{
        width: 100%
      }
    }
  }
}
</style>
