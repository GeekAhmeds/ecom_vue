<template>
  <div class="wrapper">

  <nav class="navbar is-dark">
    <router-link to="/" class="navbar-item" ><strong>E-Com</strong></router-link> 
    <a class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbar-menu" @click="showMobileMenu = !showMobileMenu">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>

    <div class="navbar-menu" id="navbar-menu" v-bind:class="{'is-active':showMobileMenu}">
      <div class="navbar-end ">
        <router-link to="/summer " class="navbar-item" >Summer</router-link> 
        <router-link to="/winter" class="navbar-item" >Winter</router-link> 

        <div class="navbar-item">
          <div class="buttons">
        <router-link to="/login " class="button is-light" >Login</router-link> 

        <router-link to="/cart " class="button is-success" >
            <spam class="icon"><i class="fas fa-shopping-cart"></i></spam>
            <span>Cart</span>
          </router-link> 
          </div>
        </div>
      </div>
    </div>
  </nav>

  <section class="section">

  <router-view/>

  </section>

    <footer class="footer">
      <p class="has-text-centerd">Copyright (c) 2023</p>
    </footer>


  </div>
</template>


<script>
  export default {
    data() {
      return {
         showMobileMenu: false,
      }
    }
  }
</script>

<style lang="scss">
@import '../node_modules/bulma';


</style>
