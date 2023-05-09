<template>
    <div class="discover-you">
        <div class="row m-3 ">
            <div class="col logo-discover d-flex justify-content-center align-items-center">
                <img src="src\assets\img\DiscoverYOU.svg" alt="">
            </div>
        </div>
        <div class="row outstand mb-5">
            <div class="col-lg-8 col-sm-12 row">
                <img src="src\assets\img\news\kvngang_mobile_web-300x160.jpg" alt="">
            </div>
            <div class="col-lg-4 col-sm-12 pl-4 mt-5 discript">
                <h3>Urbas Corluray Pack</h3>
                <h6 class="mb-4">-Sắc thu khó cưỡng-</h6>
                <p class="mt-4">Urbas Corluray Pack đem đến lựa chọn “làm mới mình” với sự kết hợp 5 gam màu mang sắc thu; phù hợp với những người trẻ năng động, mong muốn thể hiện cá tính riêng biệt khó trùng lặp.</p>
                <div class="more"> 
                    <p>Đọc thêm</p> 
                    <p>| 22.09.2020</p>
                </div>
            </div>
        </div>
        <div class="nor-outstand row">
            <div class="col-6 mb-5">
                <img src="src\assets\img\news\Mobile_Blog-1980s_0-300x160.jpg" alt="">
                <h4 class="mt-3">VINTAS SAIGON 1980s</h4>
                <p class="mb-0">Với bộ 5 sản phẩm, Vintas Saigon 1980s Pack đem đến một sự lựa chọn “cũ kỹ thú vị” cho những người trẻ sống giữa thời hiện đại nhưng lại yêu nét bình dị của Sài Gòn ngày xưa ...</p>
                <div class="more"> 
                    <p>Đọc thêm</p> 
                    <p>| 22.09.2020</p>
                </div>
            </div>
            <div class="col-6 mb-5">
                <img src="src\assets\img\news\peeping_pattas01-300x160.jpg" alt="">
                <h4 class="mt-3">SNEAKER FEST VIETNAM VÀ SỰ KẾT HỢP</h4>
                <p class="mb-0">Việc sử dụng dáng giày Vulcanized High Top của Ananas trong thiết kế và cảm hứng bắt nguồn từ linh vật Peeping - đại diện cho tinh thần xuyên suốt 6 năm qua Sneaker Fest Vietnam, chúng tôi tự tin đây sẽ là sản phẩm đáng mong chờ cho mọi “đầu giày” vào mùa hè năm nay...</p>
                <div class="more"> 
                    <p>Đọc thêm</p> 
                    <p>| 22.09.2020</p>
                </div>
            </div>
            <div class="col-6 mb-5">
                <img src="src\assets\img\news\shoes-anatomy-thumbnail-300x160.jpg" alt="">
                <h4 class="mt-3">"GIẢI PHẪU" GIÀY VULCANIZED</h4>
                <p class="mb-0">Trong phạm vi bài viết ngắn, hãy cùng nhau tìm hiểu cấu tạo giày Vulcanized Sneaker - loại sản phẩm mà Ananas đã chọn làm "cốt lõi" để theo đuổi trong suốt hành trình của mình...</p>
                <div class="more"> 
                    <p>Đọc thêm</p> 
                    <p>| 05.07.2019</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "discover-you",
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>

<style>
    .discover-you {
        
    }

    .discover-you .logo-discover img {
        width: 178px;
    }

    .discover-you .outstand {
        background-color: #f1f2f2;
    }

    .discover-you .outstand img {
        width: 100%;
    }

    .discover-you .outstand h3,
    .discover-you .outstand h6 {
        text-transform: uppercase;
        font-weight: 600;
    }

    .discover-you .more p {
        display: inline;
    }

    .discover-you .more p:first-child {
        color: #f15e2c;
        font-style: italic;
        cursor: pointer;
    }

    .discover-you .more p:last-child {
        color: #8b8b8b;
    }

    .discover-you .nor-outstand img {
        width: 100%;
        height: 300px;
        object-fit: cover;
    }

    .discover-you .nor-outstand h4 {
        font-weight: 600;
    }

    @media (max-width: 768px) {
          
    }

    @media (max-width: 1024px) {
        .discover-you .outstand .discript {
            text-align: center;
        }

        .discover-you .outstand .discript p {
            display: none;
        }

        .discover-you .nor-outstand img {
            height: 150px;
        }

        .discover-you .nor-outstand p {
            display: none;
        }
    }
</style>