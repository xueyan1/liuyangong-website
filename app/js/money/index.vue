<template>
    <div>
        <Header />
        <Mslider />
        <Ada />
        <Reward />
        <Money />
        <Adb />
        <Navbar cname="mfooter" />
    </div>
</template>

<script type="text/ecmascript-6">
import Header from "../../js/public/header.vue"
import Footer from "../../js/public/footer.vue"
import Navbar from "../../js/public/navbar.vue"
import Reward from "../home/reward.vue"
import Money from "../home/money.vue"
import Mslider from "./mslider.vue"
import Ada from "./ada.vue"
import Adb from "./adb.vue"

export default {
    components: {
        Header,
        Footer,
        Navbar,
        Mslider,
        Ada,
        Adb,
        Money,
        Reward,
    },
    data() {
        return {

        }
    },
}
</script>

<style lang="scss" module>
.mfooter {
  margin: 0 !important;
  ul {
    li:first-child {
      display: none;
    }
  }
}
</style>
