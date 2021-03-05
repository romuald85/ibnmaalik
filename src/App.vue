<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
    <div class="modal" tabindex="-1" id="myModal">
      <i class="mt-4 mr-5 bg-transparent float-right fas fa-times" data-bs-dismiss="modal" aria-label="Close"></i>
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content bg-transparent">
          <div class="modal-body bg-transparent">
            <ul class="list-group list-group-flush">
              <li v-for="tab in tabs" v-bind:key="tab.name" class="list-group-item text-center bg-transparent"><a v-bind:href="tab.href" class="text-dark text-decoration-none">{{tab.name}}</a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  <header>
    <div class="bannerbox">
      <nav class="nav1 navbar navbar-dark" aria-label="First navbar example">
        <div class="container-fluid">
          <div>
            <a class="navbar-brand text-dark" href="/">{{ title }}</a>
            <p>La clé qui ouvre la porte de la science</p>
          </div>
          <button class="navbar-toggler navbar-dark custom-toggler" type="button" data-bs-toggle="modal" data-bs-target="#myModal"
            aria-controls="navbarsExample01" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>

          <!-- <div class="collapse navbar-collapse" id="navbarsExample01">
        <ul class="navbar-nav me-auto mb-2">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="dropdown01" data-bs-toggle="dropdown" aria-expanded="false">Dropdown</a>
            <ul class="dropdown-menu" aria-labelledby="dropdown01">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
        </ul>
        <form>
          <input class="form-control" type="text" placeholder="Search" aria-label="Search">
        </form>
      </div> -->
        </div>
      </nav>
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
      const offsetHeight = nav.offsetHeight
      window.addEventListener('scroll', () => {
        if (window.scrollY >= offsetHeight) {
          nav.style.background = '#ffff'
          nav.style.position = 'fixed'
          nav.style.width = '100%'
          nav.style.top = 0
        } else {
          nav.style.position = 'static';
          nav.style.background = 'transparent'
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

  .navbar{
    background-color: transparent;
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

  .modal{
    background-color: rgba(140, 217, 241, 0.8);
  }

  .text {
    position: absolute;
    text-align: center;
    top: 40%;
    left: 0;
    right: 0;
  }

  .fa-times {
    cursor: pointer;
  }

  .close {
    cursor: pointer;
  }

  .nav1 {
    width: 100%;
    z-index: 200;
  }

  .custom-toggler .navbar-toggler-icon {
  background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 32 32' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba(44,62,80, 0.5)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 8h24M4 16h24M4 24h24'/%3E%3C/svg%3E");
}

.custom-toggler.navbar-toggler {
  border-color: rgb(44,62,80);
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