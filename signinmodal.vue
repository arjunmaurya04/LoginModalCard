<template>
<div @click="$emit('closeCard')" class="overlay" style="position: absolute;top: 0;left: 0;width: 100%;height: 100%;background: rgba(0, 0, 0, 0.5); "></div>
    <div class="card">
        <div class="back" @click="$emit('showLogin')"><strong><</strong></div>
        <span @click="$emit('closeCard')">&times;</span>
        <div class="card_top">
            <img class="logo" src="../assets/logo1.jpeg" alt="logo">
            <h2 style="font-family: Arial, Helvetica, sans-serif;">Welcome back !</h2>
            <input type="email" class="email" placeholder="Email">
            <input type="password" class="crtpss" placeholder="Password">
        </div>
        <div class="card_bottom">
            <button class="loginb">Login</button>
            <div class="sep"></div>

           <p style="font-size: 12px; font-family: Arial, Helvetica, sans-serif;margin-bottom: 20px;"> <a class='link' href="" >Forgot password?    </a> </p>
           <p style="font-size: 12px; font-family: Arial, Helvetica, sans-serif;margin-bottom: 20px;"><a  @click="$emit('showRegister')">Not yet registered? Register here</a></p>
        </div>

    </div>
</template>
<script>
export default {
    name: 'signinmodal'
}
</script>
<style scoped>
.card {
    align-items: center;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    max-width: 380px;
    width: 100%;
    text-align: center;
    font-size: 22px;
    color: black;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(1.2);
    border-radius: 12px;
    justify-content: center;
    padding: 16px;
    margin: 16px;
    background-color: white;
}

.logo {
    width: 100px;
    margin-bottom: 5px;
    margin-top: 30px;
}

span {
    position: absolute;
    right: 10px;
    top: 10px;
    cursor: pointer;
}
span:hover {
    background-color: rgb(173, 158, 158);
    border-radius: 10px;
    color: white;
    padding: 10px;
}
.back {
    position: absolute;
    left: 10px;
    top: 10px;
    cursor: pointer;
}
.back:hover {
    background-color: rgb(173, 158, 158);
    border-radius: 10px;
    color: white;
    padding: 10px; 
}
input {width: 320px;
    border: none;
    border-bottom: 2px solid rgb(198, 189, 189);
    padding: 20px;
}
input:focus {
    outline: none;
    border: none;
    border-bottom: 2px solid rgb(13, 12, 12);
    transition: 0.5s;
    transition-timing-function: ease-out;
}
input:hover {
    border-bottom: 2px solid rgb(13, 12, 12);
}
.loginb {
    margin-top: 30px;
    margin-bottom: 5px;
    background-color: rgb(110, 178, 233);
    border-radius: 15px;
    width: 100px;
    padding: 10px;
    border: none;
    color: white;
}
.loginb:hover {
    color:#000000;
}
.link {
    font-size: 12px;
    font-family: Arial, Helvetica, sans-serif;
    padding: 5px;
}
a {
    color: rgb(79, 143, 196);
    cursor: pointer;
}
</style>