<template>
    <div>
        <Header />
        <Sslider />
        <Sign />
        <Recommend />
        <More />
        <Footer />
        <Navbar cname="mfooter" />
    </div>
</template>

<script type="text/ecmascript-6">
import Header from "../../js/public/header.vue"
import Footer from "../../js/public/footer.vue"
import Navbar from "../../js/public/navbar.vue"
import Sslider from "./sslider.vue"
import Sign from "./sign.vue"
import Recommend from "./recommend.vue"
import More from "./more.vue"

export default {
    components: {
        Header,
        Footer,
        Navbar,
        Sslider,
        Sign,
        Recommend,
        More,
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
