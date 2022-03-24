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
    <hr>

    <!-- populate area between main nav and footer with content from /pages files  -->
    <Nuxt />

    <!-- footer -->
    <hr>
    <footer>

      <!-- 2 column grid layout for footer links -->
      <div class="row">
        <hr>
        <div class="col-sm">

          <!-- v-for to iterate through social links object -->
          <div v-for="social in socialLinks" v-bind:key="social.id">
            <h4>{{ social.name }}</h4>
            <ul>
              <li><a v-bind:href="social.linku1" target="_blank">{{ social.link1 }}</a></li>
              <li><a v-bind:href="social.linku2" target="_blank">{{ social.link2 }}</a></li>
              <li><a v-bind:href="social.linku3" target="_blank">{{ social.link3 }}</a></li>
            </ul>
          </div>
        </div>
        
        <div class="col-sm">

          <!-- v-for to iterate through quick links object -->
          <div v-for="quick in quickLinks" v-bind:key="quick.id">
            <h4>Box Office Bits Contributors</h4>
            <ul>
              <li>Site Author: Danika Jackson</li>
              <li>Collaborators: Steven Speicher and UW staff</li>
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
        link2: 'Movie of the Week',
        linku2: '/motw'
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
  background-color: #E0E8F9;
  color: #27241D;
  font-size: 1rem;
}

h1 {
  font-family: serif;
  font-size: 2.5rem;
  font-style: italic;
}

h2 {
  font-family: sans-serif;
  font-size: 2rem;
  font-style: italic;
  padding-top: 1rem;
}

h3 {
  font-family: sans-serif;
  font-size: 1.5rem;
  padding-top: 1.5rem;
}

nav {
  padding: 30px 0;
}

nav a {
  font-weight: bold;
  color: #035388;
}

nav a.router-link-exact-active {
  color: #8C4CCD;
}

hr {
    border: 1px solid black;
}
.body-hr {
  max-width: 75%;
  text-align: center;
  border: .5px solid #647ACB;
  margin: 10px 0;
}

footer {
  padding: 50px 0;
}
</style>
