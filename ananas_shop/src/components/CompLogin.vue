<template>
    <div class="login row p-5 text-center">
        <h1 class="col-12 mt-5 mb-5">Coming soon</h1>
        <div class="col-12">
            <p>Đăng kí ngay Email để nhận thông tin sớm nhất!</p>
            <div class="form">
                <input type="text" name="" id="">
                <button><img src="src\assets\img\icon\arrow_right.png" alt=""></button>
            </div>
            <p class="mt-5">Theo dõi chúng tôi trên các trang mạng xã hội:</p>
            <div class="col">
                <img src="src\assets\img\icon\icon_facebook.svg" class="m-1">
                <img src="src\assets\img\icon\icon_instagram.svg" class="m-1">
                <img src="src\assets\img\icon\icon_youtube.svg" class="m-1">
            </div>
            <div class="col-12 back mt-5 mb-5">
                <button v-on:click="$emit('CompCallEvent', 0)">Quay lại trang chủ</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "login"
}
</script>

<style>
    .login {
        background-image: url(../assets/img/login/bg_comingsoon.jpg);
        background-repeat: no-repeat;
        background-size: auto;
        background-position: center;
        overflow: hidden;
        /* min-height: 900px; */
        color: #fff;
    }

    .login h1 {
        text-transform: uppercase;
        font-weight: 600;
        white-space: nowrap;
        font-size: 4.5rem;
    }

    .login p {
        font-family: 'Roboto', sans-serif, Arial;
    }

    .login .form input:focus {
        outline: none;
        box-shadow:0 0 8px rgba(102, 175, 233, 0.6);
        border: 1px solid #66afe9;
    }

    .login .form input {
        height: 44px;
        width: 300px;
        
    } 
    
    .login .form button {
        height: 44px;
        width: 50px;
        border: none;
        background-color: #f15e2c;
        cursor: pointer;
    }

    .login .form button img {
        width: 28px;
    }

    .login .back button{
        height: 80px;
        width: 400px;
        border: none;
        background-color: #f15e2c;
        text-transform: uppercase;
        color: #fff;
        font-weight: 600;
        font-size: 150%;
        cursor: pointer;
    }

    @media (max-width: 1024px) {
        .login .back button{
            font-size: 100%;
        }
    }

    @media (max-width: 600px) {
        .login h1 {
            font-size: 2.5rem;
        }

        .login .back button{
            width: 200px;
        }
    }
</style>