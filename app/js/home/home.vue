<template>
    <Panel :class="$style.panel"
           title="鎏嫣宫">
        <section :class="$style.content">
            <span>鎏嫣宫 </span>
            <p>敬请期待</p>
            <Time :endTime="endTime"
                  :class="$style.time" />
        </section>

    </Panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../core/panel.vue"
import Time from "../../components/Time.vue"

export default {
    components: {
        Panel,
        Time,
    },
    data() {
        return {
            endTime: "2019/12/31 00:00:00",
        }
    },
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";
html,
body {
  background-color: #fff;
}
.panel {
  @include panel;
  margin: 0 !important;
  background-image: linear-gradient(250deg, #33d8f5 0, #2b1a19 75%);
  > h4 {
    display: none;
  }
  .content {
    @include flex;
    justify-content: flex-start;
    align-items: center;
    height: 24.5rem;
    width: 100%;
    background-image: linear-gradient(250deg, #33d8f5 0, #2b1a19 75%);
    > p {
      @include btn(
        $size: 0.6rem,
        $color: #fff,
        $bgcolor: #f1443e8c,
        $padding: 5px,
        $radius: 5px
      );
      height: 1rem;
      line-height: 1rem;
      width: 5rem;
      background-image: linear-gradient(270deg, #3397f5 0, #f18f86 75%);
      box-shadow: 0 12px 32px 0 rgba(255, 159, 135, 0.6);
      position: fixed;
      bottom: 1.5rem;
      right: 1rem;
    }
    span {
      text-shadow: 5px 5px 0 #666, 7px 7px 0 #eee;
      position: absolute;
      top: 4rem;
      font-size: 2rem;
      color: #c6b4c2;
      font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
    }
  }
  .time {
    text-shadow: none !important;
    font-size: 0.5rem !important;
    z-index: 3;
    width: 5rem;
    height: 1rem;
    position: fixed !important;
    top: 1rem !important;
    right: 1rem;
    color: #ddd !important;
  }
}
</style>
