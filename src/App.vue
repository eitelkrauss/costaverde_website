<template>
  <div id="app">
    <v-app-bar dark fixed>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <v-toolbar-title id="toolbar-title">COSTA VERDE</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text><i class="fas fa-shopping-cart"></i></v-btn>
      <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab to="/">Home</v-tab>
          <v-tab to="/shop">Shop</v-tab>
          <v-tab to="/about">About</v-tab>
        </v-tabs>
      </template>
    </v-app-bar>
    <router-view id="view" />
    <footer>
      <div id="cards-container">
        <i class="fab fa-cc-visa footer-icons"></i>
        <i class="fab fa-cc-mastercard footer-icons"></i>
      </div>
      <p id="copy">Copyright 2021. COSTA VERDE</p>
    </footer>
  </div>
</template>



<style lang="scss">
#app {
  font-family: 'Signika Negative', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: black;
  min-height: 100vh;
}

footer {
  margin-top: 2rem;
  text-align: center;
}

#view {
  margin-top: 96px;
}

#toolbar-title {
  font-family: 'Kurale';
  font-size: 1.8rem;

}

#copy {
  font-family: Arial, Helvetica, sans-serif;
}

@media (min-width: 900px) {
  #app {
    padding-right: 300px;
    padding-left: 300px;
  }

  #toolbar-title {
    font-size: 2.4rem;
  }


}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;

    &.router-link-exact-active {
      color: #62d3a0;
    }
  }
}

.footer-icons {
  font-size: 2rem;
  margin: .5rem;
}
</style>
