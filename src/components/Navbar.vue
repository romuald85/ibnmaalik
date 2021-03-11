<template>
  <div class="modal fade" tabindex="-1" id="myModal">
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
          <div class="pt-2 pl-5">
            <a class="navbar-brand text-dark" href="/">{{ title }}</a>
            <p>La clé qui ouvre la porte de la science</p>
          </div>
          <button class="mr-4 navbar-toggler navbar-dark custom-toggler" type="button" data-bs-toggle="modal" data-bs-target="#myModal"
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
        <br>
        <h2 class="big-title pt-5 pl-5 text-start second-title">Institut de langue arabe en ligne</h2>
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
</template>

<script>
  export default {
    name: 'Navbar',
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

    //   openNavPopup() {
    //     document.querySelector('.navpopup').style.position = 'static'
    //     document.querySelector('.navpopup').style.transitionDuration = '0.5s'
    //     document.querySelector('.navpopup').style.width = '100%'
    //     document.querySelector('.list-navpopup').style.display = 'block'
    //     document.querySelector('.hamburger').style.display = 'none'
    //   },
    //   closeNavPopup() {
    //     document.querySelector('.navpopup').style.position = 'absolute'
    //     document.querySelector('.navpopup').style.width = 0
    //     document.querySelector('.list-navpopup').style.display = 'none'
    //     document.querySelector('.hamburger').style.display = 'block'
    //   }
   },
    mounted() {
      document.querySelectorAll('.nav-link').forEach((tab) => {
        if (tab.href === window.location.href) {
          tab.classList.add('active')
        }
      })
      const nav = document.querySelector('.navbar')
      const bigTitle = document.querySelector('.big-title')
      const offsetHeight = nav.offsetHeight
      const offsetHeightTitle = bigTitle.offsetHeight
      window.addEventListener('scroll', () => {
        if (window.scrollY >= offsetHeight + offsetHeightTitle) {
          nav.classList.remove('nav-effects-scrollup')
          nav.classList.add('nav-effects-scrolldown')
        } else {
          nav.classList.remove('nav-effects-scrolldown')
          nav.classList.add('nav-effects-scrollup')
        }
      })
    }
  }
</script>

<style scoped>
  .navbar{
    position: fixed;
    background-color: transparent;
    width: 100%;
    z-index: 200;
  }

  .nav-effects-scrolldown{
    padding: 0 0;
    background: #fff;
    transition: all 0.4s ease-in-out;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
  }


  .nav-effects-scrollup{
    background: transparent;
    transition: all 0.4s ease-in-out;
    padding: 10px 0;
    box-shadow: 0 0 0 0;
  }


  /* .navpopup {
    background-color: rgba(140, 217, 241, 0.8);
    position: absolute;
    height: 850px;
    width: 0;
  }

  .list-navpopup {
    display: none;
  } */

  .bannerbox {
    background: linear-gradient(to bottom, #B6E3F1, #0001),
      fixed no-repeat center url("/assets/images/desert.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    height: 850px;
  }

  .modal{
    background-color: rgba(140, 217, 241, 0.8);
  }

  .modal.fade{
    transition: all 0.5s ease-in-out;
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
