<template>
    <div class="product-page">
        <div class="row">
            <div class="col-lg-3 col-xs-12 mt-5 pl-5">
                <div class="col top-left">
                    <p class="pr-3">Nam </p>
                    <p class="pr-3 pl-3">Nữ</p>
                    <p class="pl-3">Tất cả</p>
                </div>
                <hr>
                <div class="col fillter-first row">
                    <li class="col-4 col-lg-12">Accessories | Phụ kiện</li>
                    <li class="col-4 col-lg-12">Footwear | Lên chân</li>
                    <li class="col-4 col-lg-12">Top | Nửa trên</li>
                </div>
                <hr>
                <div class="col fillter d-none d-xl-block">
                    <div>Trạng thái</div>
                    <li class="row">Limited Edition </li>
                    <li class="row">Online Only</li>
                    <li class="row">Sale off</li>
                    <li class="row">New Arrival</li>
                </div>
                <div class="col fillter d-none d-xl-block">
                    <div>Kiểu dáng</div>
                    <li class="row">Low Top</li>
                    <li class="row">High Top</li>
                    <li class="row">Mid Top</li>
                    <li class="row">Mule</li>
                </div>
                <div class="col fillter d-none d-xl-block">
                    <div>Dòng sản phẩm</div>
                    <li class="row">Basas</li>
                    <li class="row">Vintas</li>
                    <li class="row">Urbas</li>
                    <li class="row">Pattas</li>
                    <li class="row">Tote Bag</li>
                    <li class="row">Graphic Tee</li>
                    <li class="row">Hoodie</li>
                    <li class="row">Sweatshirt</li>
                    <li class="row">Socks | Vớ</li>
                    <li class="row">Hat</li>
                    <li class="row">Track 6</li>
                    <li class="row">Basic Tee</li>
                    <li class="row">Shoelaces</li>
                </div>
                <div class="col fillter d-none d-xl-block">
                    <div>Giá</div>
                    <li class="row">500k - 599k</li>
                    <li class="row"> >600k</li>
                    <li class="row">400k - 499k</li>
                    <li class="row">300k - 399k</li>
                    <li class="row">200k - 299k</li>
                    <li class="row"> >200k</li>
                </div>
                <div class="col size pb-5 d-none d-xl-block">
                    <div class="title">Size giày</div>
                    <div class="row">
                        <div class="col-3 p-2 pt-3 pb-3 size-number" v-for="number in size" :key="number">{{ number }}</div>
                    </div>
                </div>
            </div>
            <div class="col-lg-9 col-xs-12 right">
                <div class="des-img mb-5">
                    <img src="src\assets\img\product\desktop_productlist.jpg" alt="" class="col-lg-12">
                </div>
                <div class="row product">
                    <div class="col-lg-4 col-6"
                        v-for="(item, index) in listProduct" 
                        v-bind:key="index">
                        <div class="img-div" >
                            <img :src="'src/assets/img/product/'+ item.img1" alt="" class="item-img1">
                            <img :src="'src/assets/img/product/'+ item.img2" alt="" class="item-img2">
                            <div class="sold-out" v-if="item.number === 0"> Hết hàng </div>
                            <div class="limited"
                                v-if="item.limited === 1">
                                Limited Edition
                            </div>
                            <div class="buy-now" v-if="item.number > 0">
                                <p>Mua ngay</p>
                            </div>
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" 
                                v-if="item.tym ===1"
                                v-on:click="tymAction(index)">
                            <path d="M47.6 300.4L228.3 469.1c7.5 7 17.4 10.9 27.7 10.9s20.2-3.9 27.7-10.9L464.4 300.4c30.4-28.3 47.6-68 47.6-109.5v-5.8c0-69.9-50.5-129.5-119.4-141C347 36.5 300.6 51.4 268 84L256 96 244 84c-32.6-32.6-79-47.5-124.6-39.9C50.5 55.6 0 115.2 0 185.1v5.8c0 41.5 17.2 81.2 47.6 109.5z"/></svg>
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"
                                v-on:click="tymAction(index)">
                            <path d="M225.8 468.2l-2.5-2.3L48.1 303.2C17.4 274.7 0 234.7 0 192.8v-3.3c0-70.4 50-130.8 119.2-144C158.6 37.9 198.9 47 231 69.6c9 6.4 17.4 13.8 25 22.3c4.2-4.8 8.7-9.2 13.5-13.3c3.7-3.2 7.5-6.2 11.5-9c0 0 0 0 0 0C313.1 47 353.4 37.9 392.8 45.4C462 58.6 512 119.1 512 189.5v3.3c0 41.9-17.4 81.9-48.1 110.4L288.7 465.9l-2.5 2.3c-8.2 7.6-19 11.9-30.2 11.9s-22-4.2-30.2-11.9zM239.1 145c-.4-.3-.7-.7-1-1.1l-17.8-20c0 0-.1-.1-.1-.1c0 0 0 0 0 0c-23.1-25.9-58-37.7-92-31.2C81.6 101.5 48 142.1 48 189.5v3.3c0 28.5 11.9 55.8 32.8 75.2L256 430.7 431.2 268c20.9-19.4 32.8-46.7 32.8-75.2v-3.3c0-47.3-33.6-88-80.1-96.9c-34-6.5-69 5.4-92 31.2c0 0 0 0-.1 .1s0 0-.1 .1l-17.8 20c-.3 .4-.7 .7-1 1.1c-4.5 4.5-10.6 7-16.9 7s-12.4-2.5-16.9-7z"/></svg>

                        </div>
                        <div class="info">
                            <p class="item-name">{{item.name}}</p>
                            <p class="item-type">{{item.type}}</p>
                            <p class="item-cost">{{ item.cost | formatPrice }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "product-page",
    data() {
        return {
            listProduct: [
                {   name: 'Vintas Jazico - High Top',
                    type: 'Royal White',
                    cost: '780000',
                    img1: 'Pro_AV00165_1.jpeg',
                    img2: 'Pro_AV00165_2.jpeg',
                    tym: 1,
                    limited: 0,
                    number: 112,
                },
                {   name: 'Urbas Corluray Mix - Low Top',
                    type: 'Corluray Mix',
                    cost: '610000',
                    img1: 'Pro_AV00174_1.jpeg',
                    img2: 'Pro_AV00174_2.jpeg',
                    tym: 0,
                    limited: 0,
                    number: 99,
                },
                {   name: 'Track 6 I.S.E.E',
                    type: 'Pure White/Icy Blue',
                    cost: '1490000',
                    img1: 'Pro_A6T012_1.jpg',
                    img2: 'Pro_A6T012_2.jpg',
                    tym: 0,
                    limited: 1,
                    number: 12,
                },
                {   name: 'Track 6 Jazico - Low Top',
                    type: 'Royal White',
                    cost: '1190000',
                    img1: 'Pro_A6T016_1.jpeg',
                    img2: 'Pro_A6T016_2.jpeg',
                    tym: 0,
                    limited: 0,
                    number: 122,
                },
                {   name: 'Urbas Love+ 22 - High Top',
                    type: 'Rustic',
                    cost: '850000',
                    img1: 'Lgbt97222-1.jpg',
                    img2: 'Lgbt1080-1.jpg',
                    tym: 0,
                    limited: 1,
                    number: 0,
                },
                {   name: 'Urbas SC - Mule',
                    type: 'Dark Purple',
                    cost: '580000',
                    img1: 'Pro_AV00098_1.jpg',
                    img2: 'Pro_AV00098_2.jpg',
                    tym: 0,
                    limited: 0,
                    number: 10,
                },
                {   name: 'Pattas Living Journey - Low Top',
                    type: 'Vaporous Gray',
                    cost: '720000',
                    img1: 'Pro_AV00189_1.jpg',
                    img2: 'Pro_AV00189_2.jpg',
                    tym: 0,
                    limited: 0,
                    number: 100,
                },
                {   name: 'Ananas "Coppy" Store Bag 001 - Black',
                    type: 'Black',
                    cost: '250000',
                    img1: 'Pro_ASTB001_1.jpeg',
                    img2: 'Pro_ASTB001_9.jpg',
                    tym: 0,
                    limited: 0,
                    number: 13,
                },
                {   name: 'Basas Workaday - Low Top',
                    type: 'Real Teal',
                    cost: '580000',
                    img1: 'Pro_AV00199_1.jpg',
                    img2: 'Pro_AV00199_2.jpg',
                    tym: 0,
                    limited: 0,
                    number: 12,
                },
            ],
            size: [35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46],
        }
    },
    methods : {
        tymAction(index) {
            this.listProduct[index].tym = this.listProduct[index].tym === 0 ? 1 : 0;
        }
        
    },
    filters: {
        formatPrice(value) {
            if (!value) return '';
            const formatter = new Intl.NumberFormat('vi-VN', {
                style: 'currency',
                currency: 'VND',
                minimumFractionDigits: 0,
            })
            return formatter.format(value).replace(/₫/g, 'VND');
        }
    },
}
</script>

<style>
    .product-page {
        width: 100%;
    }

    .product-page .top-left {
        display: flex;
        justify-content: center;
        align-items: flex-end;
        text-transform: uppercase;
        font-weight: 600;
        color: #7c7c7c;
        white-space: nowrap;
    }

    .product-page .top-left p:hover {
        color: #000;
        cursor: pointer;
    }

    .product-page .top-left p {
        border-right: 1px solid #a8a8a8;
        font-size: 1.3rem;
    }

    .product-page .top-left p:last-child {
        border: none;
    }

    .product-page .size .size-number:hover,
    .product-page li:hover {
        background-color: #e2e2e2;
        cursor: pointer;
    }

    .product-page li {
        font-family: Arial, Helvetica, sans-serif;
        width: 100%;
    }

    .product-page .fillter-first li{
        padding: 6px 0 6px 14px;
    }

    .product-page .fillter {
        border-bottom: 1px #ccc dashed;
    }

    .product-page .fillter div:hover {
        cursor: pointer;
    }

    .product-page .size .title,
    .product-page .fillter div {
        padding: 10px 0 8px 0px;
        text-transform: uppercase;
        font-weight: 600;
        color: #f15e2c;
        font-size: 1.3rem;
    }

    .product-page .size .title {
        border: none;
    }

    .product-page .size .size-number {
        text-align: center;
        border: 1px solid #ccc;
    }

    .product-page .fillter li{
        padding: 6px 0 6px 30px;
        letter-spacing: 0.1px;
    }

    .product-page .fillter li:last-child {
        margin-bottom: 20px;
    }

    .product-page .des-img {
        margin-top: 20px;
    }

    .product-page .product {
        margin: 1px;
    }

    .product-page .img-div {
        display: flex;
        justify-content: center;
        align-items: flex-end;
        position: relative;
    }

    .img-div svg:hover {
        cursor: pointer;
    }

    .img-div svg {
        position: absolute;
        width: 30px;
        height: 30px;
        bottom: 8px;
        right: 8px;
        fill: #f15e2c;
        z-index: 3;
    }

    .img-div .limited {
        position: absolute;
        white-space: nowrap;
        top: 10px;
        left: 0;
        background-color: #004e9b;
        padding: 6px;
        color: #f1f1f1;
        font-weight: 600;
        font-style: italic;
        font-size: 14px;
        z-index: 3;
    }

    .product-page .sold-out {
        background-color: rgba(5, 5, 5, 0.5);
        position: absolute;
        z-index: 2;
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: #f1f1f1;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 1.4rem;
    }

    .product-page .img-div .item-img2 {
        display: none;
    }

    .product-page .img-div:hover .item-img1 {
        display: none;
        cursor: pointer;
    }

    .product-page .img-div:hover .item-img2 {
        display: block;
        cursor: pointer;
    }

    .product-page .img-div .buy-now {
        display: none;
        position: absolute;
        bottom: 0;
        background-color: #f15e2c;
        white-space: nowrap;
        padding: 1%;
        text-align: center;
        width: 60%;
        padding: 10px 0 6px 0;
    }

    .product-page .buy-now p {
        text-transform: uppercase;
        font-weight: 600;
        color: #f1f1f1;
        font-size: 1.2 rem;
    }

    .product-page .img-div:hover .buy-now {
        display: flex;
        justify-content: center;
        align-items: flex-end;
        cursor: pointer;
    }

    .product-page .right img {
        width: 100%;
    }

    .product-page .info {
        margin-top: 20px;
        text-align: center;
        margin-bottom: 40px;
    }

    .product-page .info p {
        line-height: 16px;
    }

    .product-page .info .item-cost,
    .product-page .info .item-name {
        font-weight: 600;
    }

    @media (max-width: 768px) {
        .product-page .des-img {
            margin: 0;
        }

        .product-page .product {
            margin: 0;
        }

        .product-page .img-div:hover .buy-now {
            display: none;
        }
    }

    @media (max-width: 1024px) {
        .product-page .fillter-first {
            font-weight: 600;
            text-align: center;
        }
    }

</style>