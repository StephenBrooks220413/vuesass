<template>
  <div>
    <div class="center examplex">
      <vs-navbar target-scroll="#hide-scroll-content" hide-scroll center-collapsed v-model="active">
        <template #left>
          <img src="/logo2.png" alt="">
        </template>
        <vs-navbar-item :active="active == 'guide'" id="guide">
          <NuxtLink to="/">Home</NuxtLink>
        </vs-navbar-item>
        <vs-navbar-item :active="active == 'docs'" id="docs">
          <NuxtLink to="/about">About</NuxtLink>
        </vs-navbar-item>
        <vs-navbar-item :active="active == 'components'" id="components">
          <NuxtLink to="/service">Service</NuxtLink>
        </vs-navbar-item>
        <vs-navbar-item :active="active == 'license'" id="license">
          <NuxtLink to="/gallery">Gallery</NuxtLink>
        </vs-navbar-item>
        <template #right>
          <vs-button flat >Login</vs-button>
          <vs-button>Get Started</vs-button>
        </template>
      </vs-navbar>
      <div id="hide-scroll-content" class="square">
        <!-- code here -->
      </div>
    </div>
    <Nuxt />
    <div class="grid">
      <vs-row>
        <vs-col :w="num">
          {{ num }}
        </vs-col>
        <vs-col :w="num2">
          {{ num2 }}
        </vs-col>
        <vs-col :w="num">
          {{ num }}
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>

  <script>
  import Vue from 'vue'
  import Vuesax from 'vuesax'

  import 'vuesax/dist/vuesax.css' //Vuesax styles
  Vue.use(Vuesax, {
    // options here
  })
  export default {
    data:() => ({
      active: 'guide'
    })
  }
  </script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

a {
  text-decoration: none;
  color: grey;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
