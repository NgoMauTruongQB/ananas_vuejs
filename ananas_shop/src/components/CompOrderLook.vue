<template>
    <div class="order-look container mt-5 mb-5">
        <div class="row mb-5">
            <h2 class="col-12 text-center">TRA CỨU ĐƠN HÀNG</h2>
        </div>
        <div class="d-flex justify-content-center align-items-center">
            <div class="row from">
                <div class="col-12 mt-3 mb-3">
                    <input type="text" class="" placeholder="MÃ ĐƠN HÀNG">
                </div>
                <div class="col-12 mt-3 mb-3">
                    <input type="text" class="" placeholder="Email / Số điện thoại">
                </div>
                <div class="col-12 mt-3 mb-3">
                    <button>Tra cứu đơn hàng</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "comp-order-look",
}
</script>

<style>
    .order-look h2 {
        text-transform: uppercase;
        font-weight: 600;
        white-space: nowrap;
        font-size: 1.6rem;
    }

    .order-look input:focus {
        outline: none;
        box-shadow:0 0 8px rgba(102, 175, 233, 0.6);
        border: 1px solid #66afe9;
    }

    .order-look input::placeholder {
        color: #a3a1a1;
        font-size: 14px;
    }

    .order-look input {
        padding: 6px 6px 6px 10px;
        width: 100%;
        border: 1px solid #dbdbdb;
    }

    .order-look button {
        padding: 8px;
        width: 220px;
        border: none;
        background-color: #f15e2c;
        text-transform: uppercase;
        color: #fff;
        font-weight: 600;
        cursor: pointer;
    }

    @media (max-width: 600px) {
        .order-look button {
            width: 100%;
        }

        .order-look input {
            width: 100%;
        }
    }

</style>