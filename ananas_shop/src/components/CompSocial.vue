<template>
    <div class="social row mt-5">
        <div class="news row col-xl-12 d-flex justify-content-center align-items-center">
            <h3 class="row mb-4 mt-2">Tin tức & Bài viết</h3>
            <div class="content row pl-3">
                <div class="col-6">
                    <img src="src\assets\img\news\kvngang_mobile_web-300x160.jpg" alt="">
                    <h4 class="mt-4 mb-3">Urbas Corluray Pack</h4>
                    <p>Urbas Corluray Pack đem đến lựa chọn “làm mới mình” với sự kết hợp 5 gam màu mang sắc thu; phù hợp với những người trẻ năng động, mong muốn thể...</p>
                    <p>Đọc thêm</p>
                </div>
                <div class="col-6">
                    <img src="src\assets\img\news\Mobile_Blog-1980s_0-300x160.jpg" alt="">
                    <h4 class="mt-4 mb-3">VINTAS SAIGON 1980</h4>
                    <p>Với bộ 5 sản phẩm, Vintas Saigon 1980s Pack đem đến một sự lựa chọn “cũ kỹ thú vị” cho những người trẻ sống giữa thời hiện đại nhưng lại yêu nét...</p>
                    <p>Đọc thêm</p>
                </div>
            </div>
            <div class="content row pl-3">
                <div class="col-6">
                    <img src="src\assets\img\news\peeping_pattas01-300x160.jpg" alt="">
                    <h4 class="mt-4 mb-3">SNEAKER FEST VIETNAM VÀ SỰ KẾT HỢP</h4>
                    <p>Việc sử dụng dáng giày Vulcanized High Top của Ananas trong thiết kế và cảm hứng bắt nguồn từ linh vật Peeping - đại diện cho tinh thần xuyên...</p>
                    <p>Đọc thêm</p>
                </div>
                <div class="col-6">
                    <img src="src\assets\img\news\shoes-anatomy-thumbnail-300x160.jpg" alt="">
                    <h4 class="mt-4 mb-3">"GIẢI PHẪU" GIÀY VULCANIZED</h4>
                    <p>Trong phạm vi bài viết ngắn, hãy cùng nhau tìm hiểu cấu tạo giày Vulcanized Sneaker - loại sản phẩm mà Ananas đã chọn làm "cốt lõi" để theo đuổi trong...</p>
                    <p>Đọc thêm</p>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'Social',
    data() {
        return {

        }
    }
}
</script>

<style>
    .social .news img {
        width: 100%;
        height: 300px;
        object-fit: cover;
    }

    @media (max-width: 624px) {
        .social .news img {
            height: 150px;
        }
    }

    .social h3 {
        font-weight: 600;
        text-transform: uppercase;
    }

    .social h4:hover {
        color: #f15e2c;
    }

    .social .news p:last-child:hover {
        cursor: pointer;
    }

    .social .news p:last-child {
        color: #f15e2c;
        font-style: italic;
    }

</style>