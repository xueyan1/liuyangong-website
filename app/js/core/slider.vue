<template>
    <section :class="cname">
        <swiper :options="options"
                :not-next-tick="options.notNextTick">
            <swiper-slide v-for="(item) in items"
                          :key="item.herf">
                <router-link :to="{name:item.herf}">
                    <img :src="item.src">
                </router-link>
            </swiper-slide>
            <div v-if="options.pagination"
                 slot="pagination"
                 class="swiper-pagination" />
        </swiper>
    </section>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"

export default {
    components: {
        swiper,
        swiperSlide,
    },
    props: {
        cname: {
            type: String,
            default: "",
        },
        items: {
            type: Array,
            default() {
                return [{ herf: "", src: "" }]
            },
        },
        options: {
            type: Object,
            default() {
                return {
                    autoplay: true,
                    loop: true,
                    pagination: {
                        el: ".swiper-pagination",
                    },
                    notNextTick: false,
                }
            },
        },
    },
}
</script>
<style lang="css">
@import "~swiper/dist/css/swiper.css";
</style>
