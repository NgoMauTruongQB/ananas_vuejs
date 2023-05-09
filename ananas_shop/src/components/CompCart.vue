<template>
    <div class="cart">
        <CompEmty
        headerTitle="Giỏ hàng của bạn" 
        description="Bạn không có sẵn sản phẩm trong giỏ hàng!" 
        btnDescription="Quay lại mua hàng" 
        v-on:CompCallEvent="handleCompCallBtn"/>
    </div>
</template>

<script>
import CompEmty from "./CompEmty.vue";
export default {
    name: 'comp-cart',
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
