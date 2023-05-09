<template>
    <div class="emty mt-5 mb-5 container">
        <div class="row">
            <h2 class="col-12 text-center mt-1 pb-3">{{headerTitle}}</h2>
            <div class="col-12 text-center p-5">
                {{description}}
            </div>
            <div class="col-12 text-center" >
                <button class="refesh p-2 pl-5 pr-5" v-on:click="$emit('CompCallEvent', 1)">{{btnDescription}}</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "comp-emty",
    props: {
        headerTitle: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        },
        btnDescription: {
            type: String,
            required: true
        }
    },
    methods: {
    }
}
</script>

<style>
    .emty  h2 {
        border-bottom: 2px solid #000;
        text-transform: uppercase;
        font-weight: 600;
    }

    .emty .refesh {
        background-color: #000;
        color: #f1f1f1;
        border: none;
        text-transform: uppercase;
        font-weight: 600;
    }
</style>
