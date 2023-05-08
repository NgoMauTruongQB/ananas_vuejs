<template>
    <nav class="navbar navbar-expand-md d-flex justify-content-center align-items-center row">
        <a class="navbar-brand ml-4 mr-4 " href="#" v-on:click="$emit('CompCallEvent', 0)">
            <img src="src\assets\img\Logo_Ananas_Header.svg" alt="">
        </a>

        <div class="" id="navbarNav d-flex justify-content-center align-items-center">
            <ul class="navbar-nav ml-5 d-flex justify-content-center align-items-center ">
                <li class="nav-item">
                    <div class="d-flex align-items-center">
                        <a class="nav-link d-none d-lg-block pr-4" href="#" v-on:click="$emit('CompCallEvent', 1)"> Sản phẩm 
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"> 
                            <path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg>
                        </a>
                        <div class="line d-none d-lg-block"></div> 
                    </div>
                    <div class="sub-nav">
                        <div class="top-sub-nav-1">
                        </div>
                        <div class="container">
                            <div class="row">
                                <div class="col-lg-3 mt-5">
                                    <img src="src\assets\img\navbar\Menu_Nam.jpg" alt="">
                                    <h6 class="text-center pt-4">Cho nam</h6>
                                </div>
                                <div class="col-lg-3 mt-5">
                                    <img src="src\assets\img\navbar\Menu_Nu.jpg" alt="">
                                    <h6 class="text-center pt-4">Cho nữ</h6>
                                </div>
                                <div class="col-lg-3 mt-5">
                                    <img src="src\assets\img\navbar\Menu_Sale-off.jpg" alt="">
                                    <h6 class="text-center pt-4">Outlet sale</h6>
                                </div>
                                <div class="col-lg-3 mt-5">
                                    <img src="src\assets\img\navbar\Menu_Phu-kien.jpg" alt="">
                                    <h6 class="text-center pt-4">Phụ kiện</h6>
                                </div>
                            </div>
                            <h5 class="slogan text-center col mt-5">
                                Mọi người thường gọi chúng tôi là <h5 style="font-weight: 600; color: #fff; display: inline-block;">dứa</h5> !
                            </h5>
                        </div>
                        <div class="row">

                        </div>
                    </div>
                </li>
                <li class="nav-item">
                    <div class="d-flex align-items-center">
                        <a class="nav-link d-none d-lg-block pr-4" href="#"> 
                            Nam
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"> 
                            <path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg>
                        </a>
                        <div class="line d-none d-lg-block"></div> 
                    </div>
                    <div class="sub-nav">
                        <div class="top-sub-nav-2">
                        </div>
                        <div class="col">
                            <div class="row mt-3 mb-2">
                                <div class="col-4 ml-5 first-product">
                                    <h3 class="mt-4 mb-4">Nổi bật</h3>
                                    <div>
                                        <p>Best Saller</p>
                                        <p>New Arrival</p>
                                        <p>Sale off</p>
                                    </div>
                                    <div>
                                        <h4 class="mt-4 mb-4">Bộ sản phẩm </h4>
                                        <p 
                                            v-for="(item, index) in listProductSet" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                </div>
                                <div class="col-3 ml-5">
                                    <h3 class="mt-4 mb-4">Giày</h3>
                                    <p
                                        v-for="(item, index) in listProduct" 
                                        v-bind:key="index">
                                        {{item.text}}
                                    </p>
                                    <h3 class="mt-4 mb-4">Style</h3>
                                    <div>
                                        <p
                                            v-for="(item, index) in listStyle" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                </div>
                                <div class="col-3 ml-5">
                                    <h3 class="mt-4 mb-4">Thời trang & phụ kiện</h3>
                                    <div>
                                        <h4 class="mt-4 mb-4">Nửa trên</h4>
                                        <p
                                            v-for="(item, index) in listUpper" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                    <div>
                                        <h4 class="mt-4 mb-4">Phụ kiện</h4>
                                        <p
                                            v-for="(item, index) in listAccessory" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </li>
                <li class="nav-item">
                    <div class="d-flex align-items-center">
                        <a class="nav-link d-none d-lg-block pr-4" href="#"> 
                            Nữ 
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"> 
                            <path d="M201.4 342.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 274.7 86.6 137.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z"/></svg>
                        </a>
                        <div class="line d-none d-lg-block"></div> 
                    </div>
                    <div class="sub-nav">
                        <div class="top-sub-nav-3">
                        </div>
                        <div class="col">
                            <div class="row mt-3 mb-2">
                                <div class="col-4 ml-5 first-product">
                                    <h3 class="mt-4 mb-4">Nổi bật</h3>
                                    <div>
                                        <p>Best Saller</p>
                                        <p>New Arrival</p>
                                        <p>Sale off</p>
                                    </div>
                                    <div>
                                        <h4 class="mt-4 mb-4">Bộ sản phẩm </h4>
                                        <p 
                                            v-for="(item, index) in listProductSet" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                </div>
                                <div class="col-3 ml-5">
                                    <h3 class="mt-4 mb-4">Giày</h3>
                                    <p
                                        v-for="(item, index) in listProduct" 
                                        v-bind:key="index">
                                        {{item.text}}
                                    </p>
                                    <h3 class="mt-4 mb-4">Style</h3>
                                    <div>
                                        <p
                                            v-for="(item, index) in listStyle" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                </div>
                                <div class="col-3 ml-5">
                                    <h3 class="mt-4 mb-4">Thời trang & phụ kiện</h3>
                                    <div>
                                        <h4 class="mt-4 mb-4">Nửa trên</h4>
                                        <p
                                            v-for="(item, index) in listUpper" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                    <div>
                                        <h4 class="mt-4 mb-4">Phụ kiện</h4>
                                        <p
                                            v-for="(item, index) in listAccessory" 
                                            v-bind:key="index">
                                            {{item.text}}
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </li>
                <li class="nav-item">
                    <div class="d-flex align-items-center">
                        <a class="nav-link d-none d-lg-block pr-4" href="#"> 
                            Sale off 
                        </a>
                        <div class="line d-none d-lg-block"></div> 
                    </div>
                </li>
                <li class="nav-item">
                    <a class="nav-link d-none d-lg-block pr-4" href="#">
                        <img src="src\assets\img\DiscoverYOU.svg" alt="">
                    </a>
                </li>
            </ul>
            <ul class="navbar-nav ml-5 d-flex justify-content-center align-items-center">
                <li class="nav-item">
                    <a class="nav-link d-flex d-lg-none col ml-2" href="#">
                        <img src="src\assets\img\icon\mb_search.png" alt="">
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link d-flex d-lg-none ml-2" href="#">
                        <img src="src\assets\img\icon\mb_location.png" alt="">
                    </a>
                </li>
                <li class="nav-item">
                    <a class="nav-link d-flex d-lg-none ml-2" href="#">
                        <img src="src\assets\img\icon\mb_cart.png" alt=""> (0)
                    </a>
                </li>
            </ul>
        </div>
        <div class="search d-flex justify-content-center align-items-center pl-5 d-none d-lg-block ">
            <input type="text" class="p-1 d-none d-lg-block" placeholder="Tìm kiếm">
        </div>
        <div class="show-hide d-flex justify-content-center align-items-center d-flex d-lg-none"
            v-on:click="displaySubnavActive">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"
                v-if="displaySubnav === 0">
            <path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"
                v-if="displaySubnav === 1">
            <path d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"/></svg>
        </div>
        <div class="sub-nav-sm d-flex d-lg-none"
            v-if="displaySubnav === 1">
            <div class="container">
                <div class="col-12 subnav-nav-sm">
                    <li>Sản phẩm</li>
                    <li>Dành cho nam</li>
                    <li>Dành cho nữ</li>
                    <li>Sale off</li>
                </div>
                <div class="col-12 ">
                    <li>Discover YOU</li>
                </div>
                <div class="col-12 contact">
                    <li>
                        <img src="src\assets\img\icon\icon_tra_cuu_don_hang.svg" alt="" class="ml-2 mr-2">
                        <span class="mr-2">Tra cứu đơn hàng</span>
                    </li>
                    <li>
                        <img src="src\assets\img\icon\icon_tim_cua_hang.svg" alt="" class="ml-2 mr-2">
                        <span class="mr-2">Tìm cửa hàng</span>
                    </li>
                    <li>
                        <img src="src\assets\img\icon\icon_heart_header.svg" alt="" class="ml-2 mr-2">
                        <span class="mr-2">Yêu thích</span>
                    </li>
                    <li>
                        <img src="src\assets\img\icon\icon_dang_nhap.svg" alt="" class="ml-2 mr-2">
                        <span class="mr-2">Đang nhập</span>
                    </li>
                    <li>
                        <img src="src\assets\img\icon\icon_gio_hang.svg" alt="" class="ml-2 mr-2">
                        <span class="mr-5">Giỏ hàng (0)</span>
                    </li>
                </div>
                <div class="col-12 mt-4 mb-4 d-flex justify-content-center align-items-center">
                    <h3 style="color: #ccc;">Mọi người thường gọi chúng tôi là <h2 style="font-weight: 600; color: #fff; display: inline-block;">dứa</h2> !</h3>
                </div>
            </div>
        </div>
    </nav>
    
</template>

<script>
export default {
    name: "navbar",
    data() {
        return {
            listProduct: [
                {text: 'Basas'},
                {text: 'Vintas'},
                {text: 'Urbas'},
                {text: 'Pattas'},
                {text: 'Creas'},
                {text: 'Track 6'},
            ],
            listStyle: [
                {text: 'High Top'},
                {text: 'Low Top'},
                {text: 'Slip-on'},
            ],
            listUpper: [
                {text: 'Basic Tee'},
                {text: 'Graphic Tee'},
                {text: 'Sweatshirt'},
                {text: 'Hoodie'},
            ],
            listAccessory: [
                {text: 'Nón'},
                {text: 'Giây giày'},
                {text: 'Vớ'},
                {text: 'Balo & Túi'},
            ],
            listProductSet: [
                {text: 'Pattas Living Journey'},
                {text: 'Pattas Polka Dots'},
                {text: 'Basas Evergreen'},
                {text: 'Urbas Ruler'},
                {text: 'Track 6 Class E'},
            ],
            displaySubnav: 0,
        }
    },
    methods: {
        displaySubnavActive() {
            if (this.displaySubnav === 1) this.displaySubnav = 0;
            else this.displaySubnav = 1;
        }
    }
}
</script>

<style>
    .navbar-nav h3, .navbar-nav h4, .navbar-nav p {
        white-space: nowrap;
    }

    .navbar-nav {
        position: relative;
    }

    .navbar a {
        cursor: pointer;
    }

    .navbar .navbar-brand img {
       width: 3rem;
    }

    .navbar .navbar-nav {
        display: flex;
        flex-direction: row;
    }

    .navbar .nav-item {
        width: 100%;
    }

    .navbar .nav-item a:hover {
        color: #f15e2c;
    }

    .nav-link svg {
        fill: #000;
    }

    .nav-item a:hover svg {
        fill: #f15e2c;
        transform: rotate(-180deg);
    }

    .navbar .nav-item a {
        text-transform: uppercase;
        color: #000 ;
        font-weight: 600;
        font-size: 22px;
        white-space: nowrap;
    }

    .navbar .nav-item .line {
        border-left: 2px solid #c4c4c4;
        padding: 10px;
        display: inline-block;
    }

    .navbar .search input:focus {
        outline: none;
        box-shadow:0 0 8px rgba(102, 175, 233, 0.6);
        border: 1px solid #66afe9;
    }

    .navbar .search input {
        border: 1px solid #c4c4c4;
        width: 99%;
    }

    input::placeholder {
        font-size: 12px;
        padding-left: 20px;
    }

    .show-hide svg {
        width: 60%;
        height: 40%;
        fill: #fff;
    }

    .navbar .sub-nav {
        position: fixed;
        width: 100%;
        height: 78%;
        background-color: #666;
        z-index:10;
        bottom: 0;
        left: 0;
        right: 0;
    }

    .show-hide {
        display: inline-block;
        cursor: pointer;
        background-color: #333;
        position: absolute;
        right: 0;
        top: 0;
        bottom: 0;
        width: 10%;
        z-index: 9;
    }

    .sub-nav-sm {
        position: fixed;
        width: 100%;
        height: 86%;
        background-color: #333;
        z-index:10;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: 9;
        overflow: auto;
    }

    .sub-nav-sm li:hover {
        cursor: pointer;
        color: #f15e2c;
    }

    .sub-nav-sm li {
        list-style: none;
        font-size: 1.4rem;
        font-weight: 600;
        padding: 6%;
        color: #f1f1f1;
        word-spacing: 2px;
    }

    .sub-nav-sm .subnav-nav-sm li {
        border-bottom: 1.5px dashed #8a8a8a;
        text-transform: uppercase;
    }

    .sub-nav-sm .contact {
        border-top: 2px solid #8a8a8a;
        border-bottom: 2px solid #8a8a8a;
    }

    .sub-nav-sm .contact li {
        padding: 2.5% 0;
    }

    .top-sub-nav-1 {
        position: fixed;
        width: 100px;
        height: 30px;
        bottom: 78%;
        left: 22%;
        background-color: rgba(5, 5, 5, 0);
        background-clip: padding-box;
        padding: 10px;
    }

    .top-sub-nav-2 {
        position: fixed;
        width: 100px;
        height: 30px;
        bottom: 78%;
        left: 33%;
        background-color: rgba(5, 5, 5, 0);
        background-clip: padding-box;
        padding: 10px;
    }

    .top-sub-nav-3 {
        position: fixed;
        width: 130px;
        height: 30px;
        bottom: 78%;
        left: 40%;
        background-color: rgba(5, 5, 5, 0);
        background-clip: padding-box;
        padding: 10px;
    }

    .navbar .sub-nav .first-product {
        border-right: 2px dashed #ccc;
    }

    .navbar .sub-nav h3:hover,
    .navbar .sub-nav h4:hover,
    .navbar .sub-nav p:hover {
        color: #f15e2c;
        cursor: pointer;
    }

    .navbar .sub-nav h3 {
        text-transform: uppercase;
        font-weight: 600;
        font-size: 1.5rem;
        color: #fff;
    }

    .navbar .sub-nav h4 {
        font-size: 1.3rem;
        font-weight: 600;
        color: #f1f1f1;
    }

    .navbar .sub-nav p {
        color: #ccc;
        line-height: 14px;
        font-family: 'Roboto', sans-serif;
    }

    .nav-item .sub-nav img:hover {
        filter: brightness(1);
    }

    .nav-item .sub-nav img {
        width: 100%;
        filter: brightness(0.8);
    }

    .nav-item .sub-nav h6 {
        text-transform: uppercase;
        font-weight: 600;
        font-size: 22px;
        color: #f1f1f1;
    }

    .nav-item .sub-nav h6:hover {
        color: #f15e2c;
        cursor: pointer;
    }

    .nav-item .slogan {
        font-family: 'Roboto', sans-serif;
        text-transform: uppercase;
        color: #ccc;
    }

    .sub-nav:hover,
    .nav-item:hover .sub-nav {
        display: block;
    }

    .sub-nav {
        display: none;
    }

    

    @media (max-width: 768px) {
        .navbar .navbar-brand img {
            width: 2rem;
        }

        .navbar .nav-item img {
            width: 2rem;
            display: inline;
        }

        .navbar-nav {
            flex-wrap: nowrap;
        }

        .show-hide {
            width: 20%;
        }
    }

    @media (min-width: 768px) and (max-width: 1024px){
        .sub-nav-sm {
            height: 78%;
        }
    }

</style>