<template>
  <div class="navbar">
    <div class="nav-menu">
      <nav>
        <img class="logo" alt="Vue logo" src="../assets/logo.svg" />
        <img v-if="!showMobileMenu" class="i" src="../assets/menu-icon.png" @click="showMenu()" />
        <img v-else class="i" src="../assets/icons8-close.svg" width="35" @click="showMenu()" />
        <ul class="nav-items-desktop">
          <li>About</li>
          <li>Support</li>
          <li><div class="download-button">Download</div></li>
        </ul>
      </nav>
    </div>
    <div
        class="nav-content"
        v-if="showMobileMenu"
      >
        <ul class="nav-items">
          <li>Home</li>
          <li>About</li>
          <li>Support</li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      showMobileMenu: false,
    };
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu;
    },
  },
};
</script>

<style scoped>


.nav-menu {
  padding: 25px 25px;
  border-bottom: 1px solid black;
}

.i {
  display: none;
}

nav {
}

.nav-items-desktop {
  float: right;
  font-size: 18px;
  font-weight: 500;
}

.nav-items-desktop ul {
    margin: 0;
}

.nav-items-desktop li {
    display: inline-block;
    margin-left: 80px;
}

.download-button {
    font-weight: 600;
    background-color: #fdff5e;
    border-radius: 100px;
    padding: 10px 50px;
    border: 1px solid #000;

}

.nav-content {
    display: none;
    position: absolute;
    left: 0;
    top: 90px;
    right: 0;
    bottom: 0;
    background-color: ;
  }

.nav-items {
    font-size: 50px;
    font-weight: 800;
    list-style: none;
    text-align: center;
    padding-inline-start: 0px;
}

.nav-items li {
    margin-bottom: 15px;
}

@media only screen and (max-width: 768px) {
}

@media screen and (max-width: 768px) {
  .nav-items-desktop {
    display: none;
  }

  .i {
    display: block;
    float: right;
  }

  .nav-content {
    display: block;
    background-color: #f7f5f2;
  }
}
</style>
