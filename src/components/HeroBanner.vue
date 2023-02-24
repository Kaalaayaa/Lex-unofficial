<template>
    <div class="hero-banner">
      
    </div>
  </template>
  
  <script>
  export default {
    name: "HeroBanner",
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

  .hero-banner {
    min-height: 90vh;
    background-color: lightblue;
  }


  @media screen and (max-width: 768px) {
    
  }
  </style>
  