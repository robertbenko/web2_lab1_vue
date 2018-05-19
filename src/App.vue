<template>
  <div id="app">
    <img src="./assets/logo.png">
     <h1> Witaj w systemie do zapisów na zajęcia </h1>

    <div v-if="isAuthenticated">
       <h2> zalogowany jako {{email}} </h2>
      <button @click="logOut()">Wyloguj</button>
   </div>

    <div v-else>
           <input type="email" v-model="email">
      <button @click="login()">Zaloguj</button>

    </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      email:'',
      isAuthenticated: false
    };
  },

methods: {
  login() {
    this.isAuthenticated = true;
  },

  logOut() {
    this.isAuthenticated = false;
  },
  }
};


</script>

<style lang="scss">

</style>
