<template>
<div id="app">

  <!-- use bootsrap grid layout -->
  <div class="container">

    <!-- main nav, routers to create a navigation between /views files -->
    <nav>
      <nuxt-link to="/">Home</nuxt-link> |
      <nuxt-link to="/comingSoon">Coming Soon</nuxt-link> |
      <nuxt-link to="/discoverTitles">Discover New Titles</nuxt-link> |
      <nuxt-link to="/motw">Movie of the Week</nuxt-link>
    </nav>

    <!-- populate area between main nav and footer with content from /pages files  -->
    <Nuxt />

    <!-- footer -->
    <footer>

      <!-- 2 column grid layout for footer links -->
      <div class="row">
        <hr>
        <div class="col-sm">

          <!-- v-for to iterate through quick links object -->
          <div v-for="quick in quickLinks" v-bind:key="quick.id">
            <h3>{{ quick.name }}</h3>
            <ul>
              <li><a v-bind:href="quick.linku1">{{ quick.link1 }}</a></li>
              <li><a v-bind:href="quick.linku2">{{ quick.link2 }}</a></li>
            </ul>
          </div>
        </div>
        <div class="col-sm">

          <!-- v-for to iterate through social links object -->
          <div v-for="social in socialLinks" v-bind:key="social.id">
            <h3>{{ social.name }}</h3>
            <ul>
              <li><a v-bind:href="social.linku1" target="_blank">{{ social.link1 }}</a></li>
              <li><a v-bind:href="social.linku2" target="_blank">{{ social.link2 }}</a></li>
              <li><a v-bind:href="social.linku3" target="_blank">{{ social.link3 }}</a></li>
            </ul>
          </div>
        </div>
      </div>
    </footer>
  </div>
</div>
</template>


<script>


export default {
  name: 'app',
  data() {
    return {

      // objects for quick links and social media links in footer
      quickLinks: [{
        name: 'Quick Links',
        link1: 'Coming Soon',
        linku1: '/comingSoon',
        link2: 'Archives',
        linku2: '/movieWeek'
      }],
      socialLinks: [{
        name: 'Follow Us',
        link1: 'Facebook',
        linku1: 'https://www.facebook.com/',
        link2: 'Instagram',
        linku2: 'https://www.instagram.com/',
        link3: 'Twitter',
        linku3: 'https://twitter.com/'
      }]
    }
  }
}
</script>


<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding: 0 10rem;
}

nav {
  padding: 30px 0;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #8C4CCD;
}

footer {
  padding: 50px 0;
}
</style>
