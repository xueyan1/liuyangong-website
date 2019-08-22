<template>
    <article>
        <slider :items="items"
                :cname="$style.slider" />
        <section :class="$style.list">
            <div v-for="item in enters"
                 :key="item.img"
                 :class="$style.item">
                <router-link :to="{name:item.href}">
                    <img :src="item.img"
                         :alt="item.title">
                    <h4> {{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"

export default {
    components: {
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t13744/11/2508939408/43213/58bfe502/5a421ff3N52d0a474.jpg?width=750&height=320",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t16138/325/817844900/36681/5d874455/5a422029Ncd678ea3.jpg?width=750&height=320",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t13465/324/2563794460/43029/3ffca963/5a421f83Ne8089231.jpg?width=750&height=320",
            }], // slider的数据
            enters: [
                {
                    href: "download",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                    title: "优惠券",
                }, {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                    title: "领红包",
                }, {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                    title: "抢钢镚",
                }, {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                    title: "白条提额",
                }, {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png?width=90&height=90",
                    title: "工资理财",
                },
                {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90",
                    title: "众筹",
                },
                {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t1/36242/13/119/12214/5cb06492E0c73a66f/a284f91242e27af1.png?width=90&height=90",
                    title: "免费领京豆",
                },
                {
                    href: "home",
                    img: "//img12.360buyimg.com/jrpmobile/jfs/t1/23337/6/15445/8974/5cb064c2E0cadac1d/c533bfe4da578fe7.png?width=90&height=90",
                    title: "免息红包",
                },
            ], // 按钮的数据
        }
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider {
  margin-top: 120px;
  img {
    width: 100%;
  }
}
.list {
  @include list(row);
  background: #fff;
  padding: 40px 0px 20px 0px;
  justify-content: space-around;
  a {
    text-decoration: none;
  }
  .item {
    width: 25%;
    margin-bottom: 40px;
    text-align: center;
    img {
      display: inline-block;
      width: 90px;
      height: 90px;
    }
    h4 {
      font-size: 26px;
      margin-top: 12px;
      color: #666;
    }
  }
}
</style>
