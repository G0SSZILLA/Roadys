<template>
      <nav class="navbar navbar-expand-lg navbar-light bg-info border-1">
    <router-link class="navbar-brand text-white" :to="{ name: 'Home' }"
      >Roadys</router-link>
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
      <ul class="navbar-nav mr-auto">
        <li class="nav-item" :class="{ active: $route.name == 'Home' }">
          <router-link :to="{ name: 'Home' }" class="nav-link text-white"
            >Home</router-link>
        </li>
        <li
          class="nav-item"
          v-if="$auth.isAuthenticated"
          :class="{ active: $route.name == 'Products' }">
          <router-link class="nav-link" :to="{ name: 'Products' }"
            >Products</router-link>
        </li>
      </ul>
      <span class="navbar-text">
        <button
          class="btn btn-success"
          @click="login"
          v-if="!$auth.isAuthenticated">
          Login
        </button>
        <button class="btn btn-danger" @click="logout" v-else>logout</button>
      </span>
    </div>
  </nav>
</template>


<script>
export default {
    name: 'navbar',
    data(){
        return {}
    },
    computed:{},
    methods:{},
    components:{}
}
</script>


<style scoped>

</style>