<template>
      <nav class="navbar navbar-expand-lg border-1">
    <router-link class="navbar-brand" :to="{ name: 'Home' }"> <img class="navPhoto" src="../assets/roadys_logo_web-150x90.png"></router-link>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarText"
      aria-controls="navbarText"
      aria-expanded="false"
      aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarText">
      <ul class="navbar-nav ml-3">
        <li class="nav-item" :class="{ active: $route.name == 'Home' }">
          <router-link :to="{ name: 'Home' }" class="nav-link "
            >Home</router-link>
        </li>
        <li
          class="nav-item"
          :class="{ active: $route.name == 'Products' }">
          <router-link class="nav-link" :to="{ name: 'Products' }"
            >Products</router-link>
        </li>
      </ul>
      <!-- <span class="navbar-text">
        <button
          class="btn btn-success"
          @click="login"
          v-if="!$auth.isAuthenticated">
          Login
        </button>
        <button class="btn btn-danger" @click="logout" v-else>logout</button>
      </span> -->
    </div>
  </nav>
</template>


<script>
export default {
    name: 'Navbar',
    data(){
        return {}
    },
    computed:{},
    methods:{},
    components:{}
}
</script>


<style>
.navbar{
    background-color: #bbcbe0;
    color: #1e549a;
    font-size: 1.5rem;
}
.navPhoto{
    height: 3.75rem;
    
}

</style>