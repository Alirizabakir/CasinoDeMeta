<template>
    <div class="parallax">
        <div v-for="(item, index) in bgData" :key="index" class="bg" :style="{
            backgroundImage: 'url(' + require(`../../static/img/background/parallax/r-m-${index + 1}.png`) + ')',
            '--left': item.left + '%', '--top': item.top + '%',
            '--o': '0.' + (Math.abs((index + 1) - 10) * 10 + 1)
        }">
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            bgData: [
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
                {
                    top: 0,
                    left: 0,
                },
            ],
            screenX: 0,
            screenY: 0,
        }
    },
    methods: {
        move() {
            window.addEventListener('mousemove', e => {
                if (Math.abs(this.screenX - e.screenX) >= 600 || Math.abs(this.screenY - e.screenY) >= 400) {
                    for (let index = 0; index < this.bgData.length; index++) {
                        this.bgData[index].top = 95 - Math.floor(Math.random() * 100)
                        this.bgData[index].left = 95 - Math.floor(Math.random() * 100)
                        this.screenX = e.screenX
                        this.screenY = e.screenY
                    }
                }
            });
        }
    },
    mounted() {
        this.move()
    },
}
</script>

<style lang="scss" scoped>
.parallax {
    max-width: 100%;
    overflow: hidden;

    .bg {
        position: fixed;
        top: calc(var(--top));
        left: calc(var(--left));
        z-index: 999;
        width: 60px;
        height: 60px;
        background-position: center;
        background-repeat: no-repeat;
        pointer-events: none;
        transition: all 3s ease;
        opacity: var(--o);
    }
}
</style>