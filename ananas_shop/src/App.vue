<template>
    <div id="app" class="container" >
        <CompTopHeader v-on:CompCallEvent="handleCompCall"/>
        <CompNavbar v-on:CompCallEvent="handleCompCall"/>
        <CompTextSlide/> 
        <div v-if="CompCall === 0">
            <HomePage/>
        </div>
        <div v-if="CompCall === 1">
            <ProductPage/>
        </div>
        <div v-if="CompCall === 2">
            <SaleOffPage/>
        </div>
        <div v-if="CompCall === 3">
            <CompDiscoverYou/>
        </div>
        <div v-if="CompCall === 4">
            <CompCart v-on:CompCallEvent="handleCompCall"/>
        </div>
        <div v-if="CompCall === 5">
            <CompLogin v-on:CompCallEvent="handleCompCall"/>
        </div>
        <div v-if="CompCall === 6">
            <CompFavourite v-on:CompCallEvent="handleCompCall"/>
        </div>
        <div v-if="CompCall === 7">
            <CompFindShop v-on:CompCallEvent="handleCompCall"/>
        </div>
        <div v-if="CompCall === 8">
            <CompOrderLook/>
        </div>
        <CompFooter/>
    </div>
</template>

<script>
import CompTopHeader from "./components/CompTopHeader.vue";
import CompTextSlide from "./components/CompTextSlide.vue";
import CompNavbar from "./components/CompNavbar.vue";
import HomePage from "./components/HomePage.vue";
import ProductPage from "./components/ProductPage.vue";
import SaleOffPage from "./components/SaleOff.vue";
import CompFooter from "./components/CompFooter.vue";
import CompDiscoverYou from "./components/DiscoverYou.vue";
import CompCart from "./components/CompCart.vue";
import CompLogin from "./components/CompLogin.vue";
import CompFavourite from "./components/CompFavourite.vue";
import CompFindShop from "./components/CompFindShop.vue";
import CompOrderLook from "./components/CompOrderLook.vue";
export default {
    name: "app",
    data() {
        return {
            CompCall: 0,
        };
    },
    components: {
        CompTopHeader,
        CompTextSlide,
        CompNavbar,
        HomePage,
        ProductPage,
        SaleOffPage,
        CompFooter,
        CompDiscoverYou,
        CompCart,
        CompLogin,
        CompFavourite,
        CompFindShop,
        CompOrderLook
    },
    methods: {
        handleCompCall(payload) {
            console.log("CompCallEvent triggered with payload:", payload);
            this.CompCall = payload
        },
    }
};
</script>

<style>
    * {
        box-sizing: border-box;
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

    li {
        list-style: none;
    }
</style>
