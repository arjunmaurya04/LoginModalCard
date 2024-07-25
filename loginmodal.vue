<template>
    <!-- <div><button class="bl">Login</button>
    </div> -->
    <div @click="$emit('closeCard')" class="overlay" style="position: absolute;top: 0;left: 0;width: 100%;height: 100%;background: rgba(0, 0, 0, 0.5); "></div>
    <div class="card">
        <span @click="$emit('closeCard')">&times;</span>
        <div class="card_top">
        <img class="logo" src="../assets/logo1.jpeg" alt="logo">
    
        <button class="googleb"><img class="glogo" src="../assets/glogo.png" alt=""> Continue with Google</button>
        <button class="Githubb"><img class="gitlogo" src="../assets/gitlogo.png" alt="">    Continue with Github</button>
        </div>
        <div class="card_bottom">
            <!-- <button class="registerb" @click="showRegister">Register</button> -->
            <button class="registerb" @click="$emit('showRegister')">Register</button>
            <div class="sep"></div>
            <button class="loginb" @click="$emit('showSignin')">Login</button>
        </div>
    </div>

</template>
<script>
export default {
    name: 'loginmodal',
}

</script>
<style scoped>
.bl {
    background: #5E5DF0;
    border-radius: 999px;
    box-shadow: #5E5DF0 0 10px 20px -10px;
    box-sizing: border-box;
    color: #FFFFFF;
    cursor: pointer;
    font-family: Inter, Helvetica, "Apple Color Emoji", "Segoe UI Emoji", NotoColorEmoji, "Noto Color Emoji", "Segoe UI Symbol", "Android Emoji", EmojiSymbols, -apple-system, system-ui, "Segoe UI", Roboto, "Helvetica Neue", "Noto Sans", sans-serif;
    font-size: 16px;
    font-weight: 700;
    line-height: 24px;
    opacity: 1;
    outline: 0 solid transparent;
    padding: 8px 18px;
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    width: fit-content;
    word-break: break-word;
    border: 0;
}

.bl:hover {
    background-color: gray;
    color: white;
}
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
    transform: translate(-50%,-50%) scale(1.2);
    border-radius: 12px;
    justify-content: center;
    padding: 16px;
    margin: 16px;
    background-color: white;
}
.logo {
    width: 200px;
    margin-bottom: 80px;
    margin-top: 30px;
}

.googleb {
  align-items: center;
  background-color: #FFFFFF;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 25px;
  box-shadow: rgba(0, 0, 0, 0.02) 0 1px 3px 0;
  box-sizing: border-box;
  color: rgba(0, 0, 0, 0.85);
  cursor: pointer;
  display: inline-flex;
  font-family: system-ui,-apple-system,system-ui,"Helvetica Neue",Helvetica,Arial,sans-serif;
  font-size: 15px;
  font-weight: 600;
  justify-content: center;
  padding: 2px;
  position: relative;
  transition: all 250ms;
  width: 350px;
  margin-bottom: 20px;
}

.googleb:hover,
.googleb:focus {
  border-color: rgba(0, 0, 0, 0.15);
  box-shadow: rgba(0, 0, 0, 0.1) 0 4px 12px;
  color: rgba(0, 0, 0, 0.65);
}

.googleb:hover {
  transform: translateY(-1px);
}

.googleb:active {
  background-color: #F0F0F1;
  border-color: rgba(0, 0, 0, 0.15);
  box-shadow: rgba(0, 0, 0, 0.06) 0 2px 4px;
  color: rgba(0, 0, 0, 0.65);
  transform: translateY(0);
}
.glogo {
    width: 20px;
    padding: 9px;
}
.gitlogo {
    width: 20px;
    padding: 5px;
}

.Githubb {
    width: 350px;
    color: white;
    font-weight: 600;
    background-color: black;
    border-radius: 25px;
    padding: 2px;
    justify-content: center;
    align-items: center;
    display: inline-flex;
    margin-bottom: 90px;
    cursor: pointer;
}
.loginb {
    border: transparent;
    background-color: white;
    cursor: pointer;
    float: right;
    padding-right: 50px;
    margin-bottom: 35px;
}
.registerb {
    border: transparent;
    background-color: white;
    cursor: pointer;
    float: left;
    padding-left: 50px;
    margin-bottom: 35px;
}
.sep {
    border-left: 2px solid rgb(212, 220, 212);
  height: 60px;
  position: absolute;
  right: 50%;
  margin-right: -3px;
  bottom: 10px;
  margin-bottom: 15px;
}
span {
    position:absolute;
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
</style>