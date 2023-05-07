<template>
    <div class="text-slide row">
        <div class="col d-flex justify-content-center align-items-center pt-2 pb-2">
            <div class="begin next col-lg-3 d-none d-xl-flex"
                v-on:click="setActiveSlide">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>  
            </div>
            <div class="col-lg-6 d-flex justify-content-center align-items-center">
                <div class="slide" v-if="slideActive === 0">Hàng hai tuần nhận đổi - Giày nửa năm bảo hành</div>
                <div class="slide" v-if="slideActive === 1">Buy more pay less - Áp dụng khi mua phụ kiện</div>
                <div class="slide" v-if="slideActive === 2">Buy 2 get 10% off - Áp dụng với tất cả basic tee</div>
                <div class="slide" v-if="slideActive === 3">Free shipping với hoá đơn từ 800K!</div>
            </div>
            <div class="end next col-lg-3 d-none d-xl-flex"
                v-on:click="setActiveSlide">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                <path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>  
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'text-slide',
    data() {
        return {
            slideActive: 0,
            intervalId: null,
        }
    },
    methods: {
        setActiveSlide(e) {
            this.slideActive ++;
            if( this.slideActive > 3) this.slideActive = 0;
            if (this.slideActive < 0) this.slideActive = 3;
        },
    },
    created() {
        this.intervalId = setInterval(() => {
            this.setActiveSlide();
        }, 4000);
    },
    beforeDestroy() {
        clearInterval(this.intervalId);
    },
}
</script>

<style>
    svg {
        height: 18px;
        fill: #a19f9f;
    }

    .text-slide:hover {
        cursor: pointer;
    }

    .text-slide {
        background-color: #f1f1f1;
    }

    .text-slide .next:hover svg {
        fill: #000;
    }

    .text-slide .next {
        display: inline-block;
    }

    .text-slide .begin {
        transform: rotate(180deg);
    }

    .text-slide .slide {
        display: inline-block;
        text-transform: uppercase;
        font-style: italic;
        font-weight: 600;
        letter-spacing: 1px;
        font-size: 98%;
        font-family: 'Roboto'
    }

    @media (max-width: 768px) {
        .text-slide .slide {
            font-size: 60%;
        }
    }

</style>