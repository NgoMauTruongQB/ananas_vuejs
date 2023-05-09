<template>
    <div class="find-shop">
        <CompEmty
        headerTitle="Danh sách cửa hàng" 
        description="Hiện tại chưa cập nhật được dữ liệu!" 
        btnDescription="Quay lại trang chủ" 
        v-on:CompCallEvent="handleCompCallBtn"/>
    </div>
</template>

<script>
import CompEmty from "./CompEmty.vue";
export default {
    name: 'comp-find-shop',
    components : {
        CompEmty,
    },
    methods: {
        handleCompCallBtn() {
            this.$emit('CompCallEvent', 0);
        }
    }
}
</script>

<style>
    
</style>
