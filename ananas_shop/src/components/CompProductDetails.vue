<template>
    <div class="product-details row">
        <div class="col-xs-12 col-sm-12 col-md-12 d-none d-md-flex">
            <ol class="bread-crumb row m-4">
                <div href="" class="mb-2 pr-1 "><li class="hidden-xs hidden-sm" v-on:click="$emit('CompCallEvent', 1)">Giày</li></div> 
                <li class="product-bread-crumb">| {{productSelected.name}}</li>
            </ol>
        </div>
        <div class="col-xs-12 col-md-7 ">
            <div class="wrapper-slide p-4">
                <div class="prd-detail-main-img">
                    <img :src="'src/assets/img/product/'+ productSelected.listImg[indexSlected]" alt="">
                </div>
                <div class="prd-demo-slide">
                    <div class="img-review">
                        <img v-for="(item, index) in productSelected.listImg.slice(slideIndex, slideIndex + 4)" 
                        v-bind:key="index" :src="'src/assets/img/product/' + productSelected.listImg[index + slideIndex]" 
                        v-on:click="selectImage(item)"
                        class="demo cursor col-6 col-md-3">
                    </div>
                    <a class="prev" v-on:click="plusSlides(-1)">&#10094;</a>
                    <a class="next" v-on:click="plusSlides(1)">&#10095;</a>
                </div>
            </div>
        </div>
        <div class="col-xs-12 col-md-5 mt-4">
            <div class="info">
                <div class="row">
                    <h3 class="col-12 mb-3">{{productSelected.name}} - {{ productSelected.type}}</h3>
                    <div class="col-6 name mt-3 mb-3">Mã sản phẩm: <p class="d-inline">{{productSelected.id}}</p></div>
                    <div class="col-6 mt-3 mb-3" v-if="productSelected.number === 0"> Tình trạng: <p class="d-inline">Sold out</p> </div>
                </div>
                <h4 class="cost mt-3 mb-3">{{productSelected.cost | formatPrice}}</h4>
            </div>
            <div class="buy col">
                <div class="row ">
                    <h5 class="col-6 p-0 mt-3">Size</h5>
                    <h5 class="col-6 p-0 mt-3">Số lượng</h5>
                    <button class="col-6 select d-flex mt-1 mb-3"><svg class="ml-auto my-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg></button>
                    <button class="col-6 select d-flex mt-1 mb-3"><svg class="ml-auto my-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg></button>
                    <button class="col-8 cart mt-3 mb-3 pt-3 pb-3"><h5>Thêm vào giỏ hàng</h5></button>
                    <button class="col-3 tym mt-3 mb-3 ml-auto" v-on:click="handlTym">
                        <img v-if="tym === 0" src="src\assets\img\icon\Heart_product_1.svg">
                        <img v-if="tym === 1" src="src\assets\img\icon\Heart_product_2.svg">
                    </button>
                    <button class="col-12 pay mt-3 mb-3 pt-3 pb-3"><h5>Thanh toán</h5></button>
                </div>
            </div>
            <div class="about col">
                <div class="row mt-5 mb-5">
                    <div class="header" v-on:click="handleAction1" :class="{ 'active': action1 === 1 }">
                        <h5 class="mb-5">Thông tin sản phẩm 
                            <svg class="ml-auto my-auto" :class="{ 'rotate': action1 === 1 }" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg>
                        </h5>
                    </div>
                    <div class="content mt-3"
                        v-if="action1 === 1">
                        <p>Gender: Unisex</p>
                        <p>Size run: 35 – 46</p>
                        <p>Upper: Leather/Suede</p>
                        <p>Outsole: ICY Rubber</p>
                        <p>Có kèm theo 01 chiếc túi bạc bí ẩn (?) trong mỗi hộp giày.</p>
                        <img src="src\assets\img\size\Size-chart-1-e1559209680920.jpg" alt="">
                    </div>
                </div>
                <div class="row mt-5 mb-5">
                    <div class="header" v-on:click="handleAction2" :class="{ 'active': action2 === 1 }">
                        <h5 class="mb-5">Quy định đổi sản phẩm 
                            <svg class="ml-auto my-auto" :class="{ 'rotate': action2 === 1 }" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg>
                        </h5>
                        </div>
                    <div class="content mt-3"
                        v-if="action2 === 1">
                        <p>Đối với những sản phẩm giày và thời trang thuộc phiên bản giới hạn. Vì nhiều lý do chúng tôi sẽ không áp dụng chính sách đổi hàng. Vui lòng cân nhắc kỹ trước khi quyết định mua.</p>
                    </div>
                </div>
                <div class="row mt-5 mb-5">
                    <div class="header" v-on:click="handleAction3" :class="{ 'active': action3 === 1 }">
                        <h5 class="mb-5">Bảo hành thế nào ?
                            <svg class="ml-auto my-auto" :class="{ 'rotate': action3 === 1 }" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg>
                        </h5>
                    </div>
                    <div class="content mt-3"
                        v-if="action3 === 1">
                        <p>Mỗi đôi giày Ananas trước khi xuất xưởng đều trải qua nhiều khâu kiểm tra. Tuy vậy, trong quá trình sử dụng, nếu nhận thấy các lỗi: gãy đế, hở đế, đứt chỉ may,...trong thời gian 6 tháng từ ngày mua hàng, mong bạn sớm gửi sản phẩm về Ananas nhằm giúp chúng tôi có cơ hội phục vụ bạn tốt hơn. Vui lòng gửi sản phẩm về bất kỳ cửa hàng Ananas nào, hoặc gửi đến trung tâm bảo hành Ananas ngay trong trung tâm TP.HCM trong giờ hành chính:</p>
                        <p>Địa chỉ: 170-172, Đinh Bộ Lĩnh, P.26 , Q.Bình Thạnh, TP.HCM</p>
                        <p>Hotline: 028 2211 0067</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'product-details',
    data() {
        return {
            indexSlected: 0,
            slideIndex: 0,
            action1: 1,
            action2: 0,
            action3: 0,
            tym: 0,
        }
    },
    props: {
        productSelected: {
            type: Object,
            required: true
        }
    },
    methods: {
        plusSlides(n) {
            let maxIndex;
            if (window.innerWidth <= 768) {
                maxIndex = this.productSelected.listImg.length - 2;
            } else {
                maxIndex = this.productSelected.listImg.length - 4;
            }
            const newIndex = this.slideIndex + n;
            if (newIndex >= 0 && newIndex <= maxIndex) {
                this.slideIndex = newIndex;
            }
        },
        selectImage(item) {
            const index = this.productSelected.listImg.indexOf(item);
            this.indexSlected = index;
        },
        handleAction1() {
            this.action1 = (this.action1 === 0 ) ? 1 : 0;
        },
        handleAction2() {
            this.action2 = (this.action2 === 0 ) ? 1 : 0;
        },
        handleAction3() {
            this.action3 = (this.action3 === 0 ) ? 1 : 0;
        },
        handlTym() {
            this.tym = (this.tym === 0) ? 1 : 0;
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

    a, a:hover {
        color: #000;
        text-decoration: none;
    }

    .product-details .bread-crumb {
        width: 100%;
        border-bottom: solid 3px #000;
    }

    .product-details .bread-crumb .product-bread-crumb {
        font-weight: 600;
    } 

    .product-details .prd-detail-main-img img,
    .product-details .prd-demo-slide .demo {
        width: 100%;
        border: 1px solid #fff;
    }

    .product-details .img-review .demo {
        position: relative;
        height: 100%;
        object-fit: cover;
        transition: all 0.3s ease;
    }

    .product-details .prd-demo-slide{
        padding-top: 20px;
        position: relative;
        width: 100%;
    }

    .product-details .img-review img{
        width: 100%;
        aspect-ratio: 1 / 1;
        cursor: pointer;
        border: 1px solid #fff;
        padding: 0;
    }

    .product-details .prev:hover, 
    .product-details .next:hover {
        color: #000;
    }

    .product-details .prev, 
    .product-details .next {
        position: absolute;
        cursor: pointer;
        width: auto;
        top: 50%;
        transform: translateY(-50%);
        color: white;
        font-weight: bold;
        font-size: 20px;
        border-radius: 0 3px 3px 0;
        user-select: none;
        -webkit-user-select: none;
        background-color: #8b8b8b41;
        padding: 10px;

    }

    .next {
        right: 0;
        border-radius: 3px 0 0 3px;
    }

    @media only screen and (max-width: 767px) {
        .img-review .demo:nth-child(n+3) {
            display: none;
        }
    }

    @media only screen and (min-width: 768px) {
        .img-review .demo:nth-child(n+5) {
            display: none;
        }
    }

    .product-details .info {
        border-bottom: 1px dashed #ccc;
       
    }

    .product-details .info h3{
        text-transform: uppercase;
        font-weight: 600;
    }

    .product-details .info .name {
        white-space: nowrap;
    }

    .product-details .info p {
        font-weight: 600;
    }

    .product-details .info .cost {
        font-weight: 600;
        color: #f15e2c;
    }

    .product-details .buy h5 {
        font-weight: 600;
        text-transform: uppercase;
    }

    .product-details .buy button.select {
        background-color: #fff;
        width: 100%;
        border: 1px #ccc solid;
        height: 36px;
        cursor: pointer;
    }

    .product-details .about svg,
    .product-details .buy .select svg {
        fill: #000;
    }

    .product-details .buy button.cart,
    .product-details .buy button.tym,
    .product-details .buy button.pay{
        color: #fff;
        background-color: #000;
        border: none;
        text-transform: uppercase;
        font-weight: 600;
    }

    .product-details .buy button.pay {
        background-color: #f15e2c;
    }

    .product-details .about .header {
        border-bottom: 1px dashed #ccc;
        width: 100%;
        cursor: pointer;
    }

    .product-details .about h5 {
        text-transform: uppercase;
        font-weight: 600;
        cursor: pointer;
    }

    .product-details .about .content {
        border-bottom: 1px dashed #ccc;
        width: 100%;
    }

    .header.active h5 {
        color: #f15e2c;
    }

    .header.active svg {
        transform: rotate(180deg);
        fill: #f15e2c;
    }

    .rotate {
        transition: transform 0.3s ease-in-out;
    }

</style>