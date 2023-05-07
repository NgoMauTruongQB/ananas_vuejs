<template>
  <div class="footer row">
    <div class="col row">
        <div class="col-md-3 mx-0">
            <div class="row d-none d-md-flex justify-content-center align-items-center">
                <img src="src/assets/img/Store.svg" alt="">
            </div>
            <div class="row search-store ml-1 mr-1 justify-content-center ">
                <h5>Tìm cửa hàng</h5>
            </div>
        </div>
        <div class="col-md-9">
            <div class="row about-ananas">
                <div class="col-md-3">
                    <h4>Sản phẩm</h4>
                    <p>Giày nam</p>
                    <p>Giày nữ</p>
                    <p>Thời trang & sự kiện</p>
                    <p>Sele-off</p>
                </div>
                <div class="col-md-3">
                    <h4>Về công ty</h4>
                    <p>Dứa tuyển dụng</p>
                    <p>Liên hệ nhượng quyền</p>
                    <p>Về Ananas</p>
                </div>
                <div class="col-md-3">
                    <h4>Hỗ trợ</h4>
                    <p>FAQs</p>
                    <p>Bảo mật thông tin</p>
                    <p>Chính sách chung</p>
                    <p>Tra cứu đơn hàng</p>
                </div>
                <div class="col-md-3">
                    <h4>Liên hệ</h4>
                    <p>Email góp ý</p>
                    <p>Hotline</p>
                    <p>0921 233 432</p>
                </div>
            </div>
            <div class="row social mt-4 ml-1">
                <div class="row col-md-6">
                    <div class="col-md-6 mt-1">
                        <h4 class="row">Annanas social</h4>
                        <div class="row">
                            <img src="src\assets\img\icon\icon_facebook.svg" class="m-2">
                            <img src="src\assets\img\icon\icon_instagram.svg" class="m-2">
                            <img src="src\assets\img\icon\icon_youtube.svg" class="m-2">
                        </div>
                    </div>
                    <div class="col-md-6 mt-1">
                        <h4 class="row ">Đăng kí nhận mail</h4>
                        <input type="email" class="row col p-2">
                        <img src="src\assets\img\icon\arrow_right.jpg" alt="" class="row">
                    </div>
                    <div class="row col mt-2 d-md-none d-flex justify-content-center back-to-top">
                        <a href="#"><img src="src\assets\img\icon\icon_top.png" alt=""></a>
                        <span class="ml-2">Back to top</span>
                    </div>
                </div>
                <div class="col-md-6 d-none d-lg-flex">
                    <img src="src\assets\img\Logo_Ananas_Footer.svg" alt="">
                </div>
            </div>
            <div class="row">
                <div class="col-md-3 mt-3">
                    <img src="src\assets\img\icon_bocongthuong.png" alt="" >
                </div>
                <p class="col-md-9 mt-3 from">Nhóm thực hiện: Ngô Mậu Trường, Nguyễn Gia Bảo</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name:'footer',
    data() {
        return {

        }
    }
}
</script>

<style>
    .footer {
        background-color: #4c4c4c;
        padding: 60px 0;
        color: #fff;
    }

    .footer .search-store:hover {
        cursor: pointer;
    }

    .footer .search-store {
        background-color: #f15e2c;
        text-transform: uppercase;
    }

    .footer .search-store h5 {
        line-height: 40px;
        padding: 2px;
        font-weight: 600;
        font-family: sans-serif;
    }

    .about-ananas h4 {
        font-family: sans-serif;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 20px;
        margin: 24px 0;
        cursor: pointer;
    }

    .about-ananas p:hover {
        color: #f15e2c;
        cursor: pointer;
    }

    .about-ananas p {
        color: #ccc;
        font-family: sans-serif;
        margin: 6px 0;
    }

    .social h4:hover {
        cursor: pointer;
    }

    .social h4 {
        text-transform: uppercase;
        font-weight: 600;
        font-size: 20px;
    }  
    
    .social img:hover {
        cursor: pointer;
    }

    .social input:focus {
        outline: none;
    }

    p.col-md-9.mt-3.from {
        color: #808080;
        line-height: 60px;
    }

    .social .back-to-top {
        line-height: 42px;
        font-size: 30px;
    }

</style>
