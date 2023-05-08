<template>
    <div id="app" class="container" >
        <CompTopHeader/>
        <CompNavbar v-on:CompCallEvent="handleCompCall"/>
        <CompTextSlide/> 
        <div v-if="CompCall === 0">
            <HomePage/>
        </div>
        <div v-if="CompCall === 1">
            <ProductPage/>
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
import CompFooter from "./components/CompFooter.vue";
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
        CompFooter
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
