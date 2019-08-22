<template>
    <div>
        <Header />
        <Islider />
        <Welfare />
        <Service />
        <Footer />
        <Navbar cname="mfooter" />
    </div>
</template>

<script type="text/ecmascript-6">
import Header from "../../js/public/header.vue"
import Footer from "../../js/public/footer.vue"
import Navbar from "../../js/public/navbar.vue"
import Islider from "./islider.vue"
import Welfare from "./welfare.vue"
import Service from "./service.vue"


export default {
    components: {
        Header,
        Footer,
        Navbar,
        Islider,
        Welfare,
        Service,
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
