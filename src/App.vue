<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
  <header>
    <div class="bannerbox">
      <div class="navpopup">
        <nav class="nav1 navbar navbar-expand-lg navbar-light bg-transparent d-flex">
          <div class="container-fluid">
            <div class="block-title">
              <a class="navbar-brand" href="/">{{ title }}</a>
              <p>La clé qui ouvre la porte de la science</p>
            </div>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown"
              aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <i class="hamburger fas fa-bars" v-on:click="openNavPopup"></i>
          </div>
        </nav>
        <i class="close fas fa-times" v-on:click="closeNavPopup"></i>
        <ul class="list-navpopup text-center">
          <li>vfbg</li>
          <li>fdbg</li>
          <li>bgfb</li>
          <li>vbfgbg</li>
        </ul>
      </div>
      <div class="pt-5 pl-5">
        <h2 class="pt-5 pl-5 text-start second-title">Insitut de langue arabe en ligne</h2>
      </div>
    </div>
  </header>
  <nav class="nav2 navbar navbar-light bg-light">
    <form class="container-fluid">
      <div class="input-group">
        <button class="input-group-text btn btn-outline-success" id="basic-addon1"><i
            class="fas fa-search"></i></button>
        <input type="text" class="form-control" placeholder="Username" aria-label="Username"
          aria-describedby="basic-addon1">
        <button v-on:click="closeSearch"><i class="fas fa-times"></i></button>
      </div>
    </form>
  </nav>
  <router-view />
  <div id="footer">
    <Footer />
  </div>
</template>
<script>
  import Navbar from '@/components/Navbar.vue'
  import Footer from '@/components/Footer.vue'
  export default {
    name: 'App',
    components: {
      Navbar,
      Footer
    },
    data() {
      return {
        /*title: document.querySelector('a.nav-link.active').innerText*/
        title: "Ibn Maalik | ابن مالك",
        tabs: [{
            name: "Accueil",
            href: '/'
          },
          {
            name: "Qui sommes nous",
            href: 'who-are-we'
          },
          {
            name: "Inscription",
            href: 'register'
          },
          {
            name: "Cours",
            href: 'classes'
          },
          {
            name: "Nous contacter",
            href: 'contact'
          },
        ],
      }
    },
    methods: {
      search() {
        document.querySelector('.nav1').style.display = "none"
        document.querySelector('.nav2').style.display = "block"
      },

      closeSearch() {
        document.querySelector('.nav1').style.display = "block"
        document.querySelector('.nav2').style.display = "none"
      },

      openNavPopup() {
        document.querySelector('.navpopup').style.position = 'static'
        document.querySelector('.navpopup').style.transitionDuration = '0.5s'
        document.querySelector('.navpopup').style.width = '100%'
        document.querySelector('.list-navpopup').style.display = 'block'
        document.querySelector('.hamburger').style.display = 'none'
      },
      closeNavPopup() {
        document.querySelector('.navpopup').style.position = 'absolute'
        document.querySelector('.navpopup').style.width = 0
        document.querySelector('.list-navpopup').style.display = 'none'
        document.querySelector('.hamburger').style.display = 'block'
      }
    },
    mounted() {
      document.querySelectorAll('.nav-link').forEach((tab) => {
        if (tab.href === window.location.href) {
          tab.classList.add('active')
        }
      })
      const nav = document.querySelector('.navbar')
      const offsetTop = nav.offsetTop
      window.addEventListener('scroll', () => {
        if (window.scrollY >= offsetTop) {
          nav.style.position = 'fixed'
          nav.style.width = '100%'
          nav.style.top = 0
        } else {
          nav.style.position = 'static';
        }
      })
    }
  }
</script>
<style>
  #app {
    font-family: Montserrat, Avenir, Helvetica, Arial, sans-serif;
    font-size: 18px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }

  .navpopup {
    background-color: rgba(140, 217, 241, 0.8);
    position: absolute;
    height: 850px;
    width: 0;
  }

  .list-navpopup {
    display: none;
  }

  .bannerbox {
    background: linear-gradient(to bottom, #B6E3F1, #0001),
      fixed no-repeat center url("/assets/images/desert.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    width: 100%;
    height: 850px;
  }

  .text {
    position: absolute;
    text-align: center;
    top: 40%;
    left: 0;
    right: 0;
  }

  .hamburger {
    cursor: pointer;
  }

  .close {
    cursor: pointer;
  }

  .navbar {
    /* position: fixed; */
    width: 100%;
    z-index: 200;
  }

  .nav2 {
    display: none;
  }

  .block-title {
    padding: 0 0 0 20px;
  }

  a.nav-link.active {
    border-bottom: solid 2px #198754;
  }

  a.nav-link:hover {
    border-bottom: solid 2px #198754;
  }

  a.nav-link {
    margin: 0 20px;
  }
</style>