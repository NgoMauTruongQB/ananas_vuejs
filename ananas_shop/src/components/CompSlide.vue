<template>
    <div class="slide-main row">
        <div>
            <div class="slide-img"
                v-if="slideImgActive === 0">
                <img src="src\assets\img\slide\LowHigh_Desktop-1920x1050.jpg" alt="">
            </div>
            <div class="slide-img"
                v-if="slideImgActive === 1">
                <img src="src\assets\img\slide\Hi-im-Mule_1920x1050-Desktop.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'silde-main',
    data() {
        return {
            slideImgActive : 0,
            intervalId: null,
        }
    },
    methods: {
        setActiveSlide() {
            this.slideImgActive ++;
            if( this.slideImgActive > 1) this.slideImgActive = 0;
            if (this.slideImgActive < 0) this.slideImgActive = 1;
        },
    },
    created() {
        this.intervalId = setInterval(() => {
            this.setActiveSlide();
        }, 8000);
    },
    beforeDestroy() {
        clearInterval(this.intervalId);
    },
}
</script>

<style>
    .slide-main {
        
    }

    .slide-main .slide-img img {
        width: 100%;
    }
</style>