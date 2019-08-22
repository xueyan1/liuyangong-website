<template>
    <div>
        <div :class="$style.top">
            <span>Hi~您还未登录哦</span>
            <p>立即登录</p>
        </div>
        <div :class="$style.bottom">去京东金融App签到，最高可领5钢镚</div>
        <Navbar />
    </div>

</template>

<script type="text/ecmascript-6">
import Navbar from "../public/navbar.vue"

export default {
    components: {
        Navbar,
    },
    data() {
        return {

        }
    },
}
</script>

<style lang="scss" module>
.top {
  font-size: 32px;
  display: flex;
  align-items: center;
  border-radius: 20px;
  height: 216px;
  margin: 50px 30px;
  padding: 0 20px;
  box-sizing: border-box;
  background-color: red;
  color: white;
  box-shadow: 0 1px 1px 0 rgba(253, 130, 119, 0.2);
  p {
    margin-left: 150px;
    height: 68px;
    background-color: #222;
    font-size: 28px;
    width: 150px;
    line-height: 68px;
    border-radius: 30px;
    text-align: center;
  }
}
.bottom {
  position: fixed;
  height: 2rem;
  bottom: 120px;
  width: 85%;
  left: 40px;
  font-size: 28px;
  font-family: PingFangSC-Medium;
  color: #fce6e6;
  text-align: center;
  line-height: 2rem;
  border-radius: 120px;
  box-shadow: 0 0.25rem 0.625rem 0 #f9aba7;
  background: linear-gradient(31deg, #f8563e, #e4231b);
}
</style>
