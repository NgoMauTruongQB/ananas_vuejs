<template>
    <div class="banner row mt-2">
        <div class="left col-6">
            <div class="slide-banner "
                v-if="bannerSlideActive === 0">
                <div class="slide-img">
                    <img src="src\assets\img\banner\banner-slide2.png" alt="" class="mt-5">
                    <div class="tab d-none d-lg-flex">
                        <button v-on:click="setActiveSlide">.</button>
                        <button v-on:click="setActiveSlide">.</button>
                    </div>
                </div>
                <div class="content">
                    <h3 class="mt-4">All black in black</h3>
                    <p>Mặc dù được ứng dụng rất nhiều, nhưng sắc đen lúc nào cũng toát lên một vẻ huyền bí không nhàm chán</p>
                </div>
            </div>
            <div class="slide-banner "
                v-if="bannerSlideActive === 1">
                <div class="slide-img">
                    <img src="src\assets\img\banner\banner-slide1.png" alt="" class="mt-5">
                    <div class="tab d-none d-lg-flex">
                        <button v-on:click="setActiveSlide">.</button>
                        <button v-on:click="setActiveSlide">.</button>
                    </div>
                </div>
                <div class="content">
                    <h3 class="mt-4">Bình mới rượu "mới"</h3>
                    <p>Vẫn kế thừa vẻ tối giản, nguyên bản đã được định hướng bởi cái tên, Basas mới trở lại với những cải tiến đáng giá chắc chắn sẽ đem đến một trải nghiệm thú vị như hành trình chúng tôi làm ra nó.</p>
                </div>
            </div>
        </div>
        <div class="right col-6">
            <div class="banner-img ">
                <img src="src\assets\img\banner\Banner_Sale-off-1.jpg" alt="" class="mt-5">
                <div class="content">
                    <h3 class="mt-4">Outlet sale</h3>
                    <p>Danh mục những  sản phẩm bán tại "giá tốt hơn" chỉ được bán kênh online - Online Only, chúng đã từng làm mưa làm gió một thời gian và hiện đang rơi vào tình trạng bể size, bể số.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "banner",
    data() {
        return {
            bannerSlideActive: 0,
            intervalId: null,
        }
    },
    methods: {
        setActiveSlide() {
            const buttons = document.querySelectorAll('.banner .tab button');
            buttons.forEach((button, index) => {
                if (index === this.bannerSlideActive) {
                    button.classList.add('active');
                } else {
                    button.classList.remove('active');
                }
        });
            this.bannerSlideActive ++;
            if( this.bannerSlideActive > 1) this.bannerSlideActive = 0;
            if (this.bannerSlideActive < 0) this.bannerSlideActive = 1;
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

    .banner .slide-banner img,
    .banner .banner-img img {
        width: 100%;
    }

    .banner h3:hover {
        cursor: pointer;
        color: #f15e2c;
    }

    .banner h3 {
        text-transform: uppercase;
        font-weight: 600;
    }

    .banner .slide-img {
        position: relative;
    }

    .banner .tab {
        position: absolute;
        bottom: 3%;
        left: 40%;
        display: flex;
    }

    .banner .tab button {
        margin-right: 10px;
        border: none;
        font-size: 1px;
        color: #fff;
        cursor: pointer;
        padding: 8% 100%;
    }

    .banner .tab button.active {
        background-color: #f15e2c;
    }
</style>