<template>
  <nav class="navbar is-transparent" role="navigation" aria-label="main navigation">
    <div class="container">
      <div class="navbar-brand">
          <a class="navbar-item" href="https://ithappens.gupy.io/">
            <img src="../assets/ithappens.jpg">
          </a>
          <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
      </div>
      <div id="navbarBasicExample" class="navbar-menu">
          <div class="navbar-start">
            <router-link class="navbar-item" to="/">Inicio</router-link>
            <router-link class="navbar-item" to="/about">Sobre</router-link>
            <router-link class="navbar-item" to="/vagas">Vagas</router-link>
            <div class="navbar-item has-dropdown is-hoverable">
              <a class="navbar-link">
                Informações
              </a>
              <div class="navbar-dropdown">
                <a class="navbar-item">
                  About
                </a>
                <a class="navbar-item">
                  Jobs
                </a>
                <a class="navbar-item">
                  Contact
                </a>
                <hr class="navbar-divider">
                <a class="navbar-item">
                  Report an issue
                </a>
              </div>
            </div>
          </div>
          <div class="navbar-end">
            <div class="navbar-item">
              <div class="buttons">
                <a class="button is-primary">
                  <strong>Cadastro</strong>
                </a>
                <a class="button is-light">
                  Log in
                </a>
              </div>
            </div>
          </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>
