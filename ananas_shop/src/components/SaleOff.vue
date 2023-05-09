<template>
    <div class="sale-off-page">
        <div class="row">
            <div class="col-12 img-full">
                <img src="src\assets\img\product\Clearance-Sale-Desktop.jpg" alt="">
            </div>
            <div class=" mt-5 col-12">
                <div class="row product">
                    <div class="col-lg-4 col-6"
                        v-for="(item, index) in listProduct" 
                        v-bind:key="index">
                        <div class="img-div" >
                            <img :src="'src/assets/img/product/'+ item.img1" alt="" class="item-img1">
                            <img :src="'src/assets/img/product/'+ item.img2" alt="" class="item-img2">
                            <div class="sold-out" v-if="item.number === 0"> Hết hàng </div>
                            <div class="online"
                                v-if="item.online === 1">
                                Online Only 
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
                            <div class="sale-title mb-4 pb-2">{{ item.saleTitile }}</div>
                            <p class="item-name mt-2">{{item.name}}</p>
                            <p class="item-type">{{item.type}}</p>
                            <div class="item-cost"> {{ item.cost | formatPrice}} <div class="cost-sale">{{item.costSale | formatPrice}}</div> </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'sale-off-page',
    data() {
        return {
            listProduct: [
                {   name: 'Urbas The Gang - Low Top',
                    type: 'Haute Black',
                    cost: '350000',
                    costSale: '450000',
                    img1: 'pro_urbas_A61050_1-1.jpg',
                    img2: 'pro_urbas_A61050_2-1.jpg',
                    tym: 1,
                    online: 1,
                    number: 112,
                    saleTitile: 'Online Only',
                },
                {   name: 'Vintas Temperate - High Top',
                    type: 'Dusty Olive',
                    cost: '610000',
                    costSale: '500000',
                    img1: 'pro_A61111_1.jpg',
                    img2: 'pro_A61111_2.jpg',
                    tym: 0,
                    online: 1,
                    number: 99,
                    saleTitile: 'Sale off',
                },
                {   name: 'Urbas Bloody - Low Top',
                    type: 'Haute Red',
                    cost: '440000',
                    costSale: '400000',
                    img1: 'pro_urbas_A61054_1.jpg',
                    img2: 'pro_urbas_A61054_2.jpg',
                    tym: 0,
                    online: 1,
                    number: 12,
                    saleTitile: 'Online Only',
                },
                {   name: 'Track 6 Jazico - Low Top',
                    type: 'Royal White',
                    cost: '1190000',
                    costSale: '400000',
                    img1: 'pro_A61089_1_1.jpg',
                    img2: 'pro_A61089_7.jpg',
                    tym: 0,
                    online: 1,
                    number: 122,
                    saleTitile: 'Online Only',
                },
                {   name: 'Urbas Love+ 22 - High Top',
                    type: 'Rustic',
                    cost: '850000',
                    costSale: '680000',
                    img1: 'pro_A61093_1_1.jpg',
                    img2: 'pro_A61093_7.jpg',
                    tym: 0,
                    online: 1,
                    number: 0,
                    saleTitile: '',
                },
                {   name: 'Urbas SC - Mule',
                    type: 'Dark Purple',
                    cost: '580000',
                    costSale: '500000',
                    img1: 'pro_A61111_1.jpg',
                    img2: 'pro_A61111_2.jpg',
                    tym: 0,
                    online: 1,
                    number: 10,
                    saleTitile: '',
                },
            ]
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
    methods : {
        tymAction(index) {
            this.listProduct[index].tym = this.listProduct[index].tym === 0 ? 1 : 0;
        }
        
    },
}
</script>

<style>
    .sale-off-page {
        width: 100%;
    }
    .sale-off-page .img-full {
        display: flex;
        justify-content: center;
        align-items: flex-end;
    }

    .sale-off-page .img-full img {
        max-width: 1200px;
        height: 300px;
        object-fit: cover;
    } 

    .sale-off-page .product img {
        width: 100%;
    }

    .sale-off-page .product {
        margin: 1px;
    }

    .sale-off-page .img-div {
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

    .img-div .online {
        position: absolute;
        white-space: nowrap;
        top: 32px;
        left: 0;
        background-color: #3a3939;
        padding: 4px 30px;
        color: #f1f1f1;
        font-weight: 600;
        font-style: italic;
        font-size: 14px;
        z-index: 3;
    }

    .sale-off-page .sold-out {
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

    .sale-off-page .sale-title {
        border-bottom: 1px dashed #ccc;
    }

    .sale-off-page .img-div .item-img2 {
        display: none;
    }

    .sale-off-page .img-div:hover .item-img1 {
        display: none;
        cursor: pointer;
    }

    .sale-off-page .img-div:hover .item-img2 {
        display: block;
        cursor: pointer;
    }

    .sale-off-page .img-div .buy-now {
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

    .sale-off-page .buy-now p {
        text-transform: uppercase;
        font-weight: 600;
        color: #f1f1f1;
        font-size: 1.2 rem;
    }

    .sale-off-page .img-div:hover .buy-now {
        display: flex;
        justify-content: center;
        align-items: flex-end;
        cursor: pointer;
    }

    .sale-off-page .right img {
        width: 100%;
    }

    .sale-off-page .info {
        margin-top: 20px;
        text-align: center;
        margin-bottom: 40px;
    }

    .sale-off-page .info p {
        line-height: 16px;
    }

    .sale-off-page .info p:first-child:hover {
        cursor: pointer;
        color: #f15e2c;
    }

    .sale-off-page .info .item-cost,
    .sale-off-page .info .item-name {
        font-weight: 600;
    }

    .sale-off-page .info .cost-sale {
        margin-left: 5px;
        font-weight: 500;
        color: #8d8b8b;
        font-size: 14px;
        text-decoration: line-through;
    }

    @media (max-width: 768px) {
        .sale-off-page .img-full img {
            width: 100%;
            height: 100%;
            min-height: 150px;
            min-width: 428px;
            object-fit: cover;
            
        }

        .img-div .online {
            top: 20px;
            left: 0;
            padding: 4px 10px;
            font-size: 12px;
            z-index: 3;
        }

        .sale-off-page .img-div:hover .buy-now {
            display: none;
        }

        .sale-off-page .info .item-cost,
        .sale-off-page .info .cost-sale {
           /* display: block; */
           font-size: 12px;
        }
    }
</style>