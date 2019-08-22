/* eslint-disable radix */

<template>
    <span>{{ time }}</span>
</template>


<script>
export default{
    props: {
        endTime: {
            type: String,
            default: "",
        },
    },
    data() {
        return {
            time: "",
            flag: false,
        }
    },
    mounted() {
        const time = setInterval(() => {
            if (this.flag === true) {
                clearInterval(time)
            }
            this.timeDown()
        }, 500)
    },
    methods: {
        timeDown() {
            const endTime = new Date(this.endTime)
            const nowTime = new Date()
            // eslint-disable-next-line radix
            const leftTime = parseInt((endTime.getTime() - nowTime.getTime()) / 1000)
            // eslint-disable-next-line radix
            const d = parseInt(leftTime / (24 * 60 * 60))
            // eslint-disable-next-line radix
            const h = this.formate(parseInt(leftTime / (60 * 60) % 24))
            // eslint-disable-next-line radix
            const m = this.formate(parseInt(leftTime / 60 % 60))
            // eslint-disable-next-line radix
            const s = this.formate(parseInt(leftTime % 60))

            if (leftTime <= 0) {
                this.flag = true
                this.$emit("time-end")
            }
            this.time = `${d}天${h}小时${m}分${s}秒`     // 需要修改时间样式的话 ，比如需要什么30分钟倒计时，就只保留分和秒
        },
        formate(time) {
            if (time >= 10) {
                return time
            }
            return `0${time}`
        },
    },
}
</script>

<style lang="scss" scoped>
</style>
