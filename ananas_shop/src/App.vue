<template>
    <div id="app" class="container" >
        <CompTopHeader/>
        <CompNavbar/>
        <CompTextSlide/>  
        <CompSlideMain/>
        <CompBanner/>
        <CompHomeBuy/>
        <CompSocial/>
        <CompFooter/>
    </div>
</template>

<script>
import CompTopHeader from "./components/CompTopHeader.vue";
import CompTextSlide from "./components/CompTextSlide.vue";
import CompNavbar from "./components/CompNavbar.vue";
import CompSlideMain from "./components/CompSlide.vue";
import CompBanner from "./components/CompBanner.vue";
import CompHomeBuy from "./components/CompHomeBuy.vue";
import CompSocial from "./components/CompSocial.vue";
import CompFooter from "./components/CompFooter.vue";
export default {
    name: "app",
    data() {
        return {};
    },
    components: {
        CompTopHeader,
        CompTextSlide,
        CompNavbar,
        CompSlideMain,
        CompBanner,
        CompHomeBuy,
        CompSocial,
        CompFooter,
    },
};
</script>

<style>
    * {
        font-family: sans-serif, Arial, Helvetica;
        margin: 0;
        padding: 0;
    }

    #app {
        max-width: 100%;
        overflow: hidden;
    }

    @media screen and (max-width: 600px) {
        h3 {
            font-size: 18px;
        }

        p {
            font-size: 14px;
        }
    }
</style>
