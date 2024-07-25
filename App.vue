<script>

import loginmodal from './components/loginmodal.vue';
import registermodal from './components/registermodal.vue';
import signinmodal from './components/signinmodal.vue';
import home from './components/home.vue';

export default {
  name: 'App',
  components: {
    loginmodal,
    registermodal,
    signinmodal,
    home
  },
  

  data() {
    return {
      isHomeVisible: false,
      isLoginVisible: false,
      isRegisterVisible: false,
      isSigninVisible: false
    }
  },
  methods: {
    showHome() {
      this.isHomeVisible = true;
      this.isLoginVisible = false;
      this.isRegisterVisible = false;
      this.isSigninVisible = false;
    },
    showLogin() {
      this.isHomeVisible = false;
      this.isLoginVisible = true;
      this.isRegisterVisible = false;
      this.isSigninVisible = false;
    },
    showRegister() {
      this.isHomeVisible = false;
      this.isLoginVisible = false;
      this.isRegisterVisible = true;
      this.isSigninVisible = false;
    },
    showSignin() {
      this.isHomeVisible = false;
      this.isLoginVisible = false;
      this.isRegisterVisible = false;
      this.isSigninVisible = true;
    },
    closeCard() {
      this.isHomeVisible = false;
      this.isLoginVisible = false;
      this.isRegisterVisible = false;
      this.isSigninVisible = false;
    }
  }
}


</script>

<template>
  
  <div><button class="bl" @click="showLogin">Login</button>
  </div>


  <home v-if="isHomeVisible" />
  
  <loginmodal v-if="isLoginVisible" @showRegister="showRegister" @showSignin="showSignin" @closeCard="closeCard"/>
  <registermodal v-if="isRegisterVisible" @showSignin="showSignin" @closeCard="closeCard" @showLogin="showLogin"/>
  <signinmodal v-if="isSigninVisible" @showRegister="showRegister" @closeCard="closeCard" @showLogin="showLogin"/>
</template>

<style scoped></style>
