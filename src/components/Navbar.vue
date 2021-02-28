<template>
  <nav class="nav1 navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <div>
        <a class="navbar-brand" href="/">{{ title }}</a>
        <p>Institut de langue arabe en ligne</p>
      </div>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavDropdown"
        aria-controls="navbarNavDropdown"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse d-flex justify-content-end" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item d-flex">
            <a
              class="nav-link active"
              v-bind:href="tab.href"
              v-for="tab in tabs"
              v-bind:key="tab.name"
              >{{ tab.name }}</a>
          </li>
        </ul>
      </div>
      <button class="btn btn-outline-success" v-on:click="search"><i class="fas fa-search"></i></button>
    </div>
  </nav>
  <div class="container">
    <nav class="nav2 navbar navbar-light bg-light">
    <form class="container-fluid">
      <div class="input-group">
        <button class="input-group-text btn btn-outline-success" id="basic-addon1"><i class="fas fa-search"></i></button>
        <input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
        <button v-on:click="closeSearch"><i class="fas fa-times"></i></button>
      </div>
    </form>
</nav>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      title: "Ibn Maalik | ابن مالك",
      tabs: [
        {name: "Accueil", href: '/'},
        {name: "Qui sommes nous", href: 'who-are-we'},
        {name: "Inscription", href: 'register'},
        {name: "Cours", href: 'classes'},
        {name: "Nous contacter", href: 'contact'},
      ],
    };
  },
  methods: {
    search() {
      document.querySelector('.nav1').style.display = "none"
      document.querySelector('.nav2').style.display = "block"
    },

    closeSearch() {
      document.querySelector('.nav1').style.display = "block"
      document.querySelector('.nav2').style.display = "none"
    }
  }
};
</script>

<style scoped>
  .nav2{
    display: none;
  }

  a.nav-link:hover{
    border-bottom: solid 2px #198754;
  }
</style>
