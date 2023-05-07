<template>
    <div class="home-buy row d-flex justify-content-center align-items-center mt-5 pb-2">
        <h1 class="mb-5">Danh mục mua hàng</h1>
        <div class="row">
            <div class="col-md-4 d-flex justify-content-center align-items-center">
                <img src="src\assets\img\banner\catalogy-1.jpg" alt="" class="mt-1">
                <div class="text d-flex justify-content-center align-items-center">
                    <h4>Giày nam</h4>
                    <p>New Arrivals</p>
                    <p>Best Seller</p>
                    <p>Sale-off</p>
                </div>
            </div>
            <div class="col-md-4 d-flex justify-content-center align-items-center">
                <img src="src\assets\img\banner\catalogy-2.jpg" alt="" class="mt-1">
                <div class="text d-flex justify-content-center align-items-center">
                    <h4>Giày nữ</h4>
                    <p>New Arrivals</p>
                    <p>Best Seller</p>
                    <p>Sale-off</p>
                </div>
            </div>
            <div class="col-md-4 d-flex justify-content-center align-items-center">
                <img src="src\assets\img\banner\catalogy-3.jpg" alt="" class="mt-1">
                <div class="text d-flex justify-content-center align-items-center">
                    <h4>Dòng sản phẩm</h4>
                    <p 
                        v-for="(item, index) in listProduct" 
                        v-bind:key="index">
                        {{item.text}}
                    </p>
                </div>
            </div>
        </div>
        <div class="banner-clothing row mt-5">
            <img src="src\assets\img\banner\Banner_Clothing.jpg" alt="" class="mt-4">
        </div>
    </div>
</template>

<script>
export default {
    name: "home-buy",
    data() {
        return {
            listProduct: [
                {text: 'Basas'},
                {text: 'Vintas'},
                {text: 'Urbas'},
                {text: 'Pattas'},
            ],
        }
    }
}
</script>

<style>
    .home-buy {
        overflow: hidden;
    }
    .home-buy h1{
        text-transform: uppercase;
        font-size: 2rem;
        font-weight: 600;
    }

    .home-buy img {
        display: block;
        z-index: 0;
        width: 100%;
        filter: brightness(0.7);
    }

    .home-buy .text {
        position: absolute;
        flex-direction: column;
        height: 100%;
    }

    .home-buy .text h4:hover,
    .home-buy .text p:hover {
        color: #f15e2c;
        cursor: pointer;
    }

    .home-buy .text h4 {
        font-family: sans-serif;
        text-transform: uppercase;
        font-weight: 600;
        color: #fff;
        margin-bottom: 10%;
    }

    .home-buy .text p {
        font-family: sans-serif;
        font-weight: 600;
        color: #fff;
        line-height: 20px;
    }

    .home-buy .banner-clothing img {
        filter: brightness(1);
    }
</style>