<template>
    <div class="home-page">
        <CompSlideMain/>
        <CompBanner/>
        <CompHomeBuy/>
        <CompSocial/>
    </div>
</template>

<script>
import CompSlideMain from "./CompSlide.vue";
import CompBanner from "./CompBanner.vue";
import CompHomeBuy from "./CompHomeBuy.vue";
import CompSocial from "./CompSocial.vue";
export default {
    name: 'home-page',
    data() {
        return {}
    },
    components : {
        CompSlideMain,
        CompBanner,
        CompHomeBuy,
        CompSocial,
    }
}
</script>

<style>

</style>