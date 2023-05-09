<template>
    <div class="top-header row d-none d-md-block">
        <ul class="ml-auto d-flex justify-content-end">
            <li v-on:click="$emit('CompCallEvent', 8)">
                <img src="src\assets\img\icon\icon_tra_cuu_don_hang.svg" alt="" class="ml-2 mr-2">
                <span class="mr-2">Tra cứu đơn hàng</span>
            </li>
            <li v-on:click="$emit('CompCallEvent', 7)">
                <img src="src\assets\img\icon\icon_tim_cua_hang.svg" alt="" class="ml-2 mr-2">
                <span class="mr-2">Tìm cửa hàng</span>
            </li>
            <li v-on:click="$emit('CompCallEvent', 6)">
                <img src="src\assets\img\icon\icon_heart_header.svg" alt="" class="ml-2 mr-2">
                <span class="mr-2">Yêu thích</span>
            </li>
            <li v-on:click="$emit('CompCallEvent', 5)">
                <img src="src\assets\img\icon\icon_dang_nhap.svg" alt="" class="ml-2 mr-2">
                <span class="mr-2">Đang nhập</span>
            </li>
            <li v-on:click="$emit('CompCallEvent', 4)">
                <img src="src\assets\img\icon\icon_gio_hang.svg" alt="" class="ml-2 mr-2">
                <span class="mr-5">Giỏ hàng (0)</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "top-header",
    data() {
        return {};
    },
};
</script>

<style>
    .top-header{
        background-color: #000;
        height: 30px;
    }

    .top-header ul {
    }

    .top-header ul li {
        list-style: none;
        display: inline;
        color: #fff;
        line-height: 28px;
        font-size: 12px;
        font-family: 'Roboto';
    }

    .top-header li span {
        font-weight: 600;
    }
    .top-header li:hover span{
        cursor: pointer;
        color: #f15e2c;
    }
</style>