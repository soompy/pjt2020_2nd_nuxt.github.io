<template>
  <div class="container">
    <div>
      <header id="header">
        <ul class="gnb">
          <li><nuxt-link to="/best">Best</nuxt-link></li>
          <li><nuxt-link to="/all">All</nuxt-link></li>
          <li><nuxt-link to="/index">Coffee</nuxt-link></li>
          <li><nuxt-link to="/tea">Tea</nuxt-link></li>
          <li><nuxt-link to="/set">Set Menu</nuxt-link></li>
          <li><nuxt-link to="/bread">Bread</nuxt-link></li>
          <li><nuxt-link to="/juice">Juice</nuxt-link></li>
        </ul>
      </header>
      <logo />
      <h1 class="title">
        banapresso-order-nuxt
      </h1>
      <h2 class="subtitle">
        My smashing Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="scss" scoped>
$primaryColor: #f66b91;
// .container{min-height: auto !important;}
ul{margin: 0;padding: 0;}
li{list-style: none;}

#header{
  background: $primaryColor;
  .gnb{
    display: flex;
    li{
      flex: 1;
      text-align: center;
      a{
        display: block;
        padding: 8px 0;
        color: #fff;
        &:hover{
          font-weight: bold;
          text-decoration: none;
        }
      }
    }
  }
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

@media (max-width: 1200px){
  .container{
    max-width: 100% !important;
    padding-right: 0;
    padding-left: 0;
  }
}
</style>
