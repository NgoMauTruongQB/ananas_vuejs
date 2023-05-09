<template>
    <div class="favourite">
        <CompEmty
        headerTitle="Danh mục yêu thích" 
        description="Bạn đang không thích sản phẩm nào!" 
        btnDescription="Tiếp tục mua hàng" 
        v-on:CompCallEvent="handleCompCallBtn"/>
    </div>
</template>

<script>
import CompEmty from "./CompEmty.vue";
export default {
    name: 'comp-favourite',
    components : {
        CompEmty,
    },
    methods: {
        handleCompCallBtn(value) {
            this.$emit('CompCallEvent', value);
        }
    }
}
</script>

<style>
    
</style>
