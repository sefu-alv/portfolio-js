<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import footerComponent from './components/footerComponent.vue';
import 'primeicons/primeicons.css'
import logo from '/logo.svg'
</script>

<template>
  <header>
    
      <div class="logo-container">
        <p id="firstName">Sefufim</p>
        <span id="name">Alvarez</span>
        <img id="logo" :src="logo" alt="">
      </div>
      <input type="checkbox" id="nav_check" hidden>
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/projects">Projects</RouterLink>
          <RouterLink to="#">Contact</RouterLink>
        </nav>
        <label for="nav_check" class="hamburger">
          <div></div>
          <div></div>
          <div></div>
        </label>
      
  
  </header>

  <RouterView />
  <footerComponent/>
</template>

<style scoped>
nav{
  font-size: 30px;
  display: flex;
  gap: 20px;
  color: black;
  font-weight: 200;
  font-family:Roboto, sans-serif ;
}
header {
 width: 80%;
 height: 80px;
 background-color: #fefefe;
 display: flex;
 align-items: center;
 justify-content: space-between;
 border-radius: 0 0 10px 10px;
 padding: 0 40px;
 margin: 0 auto;
 position: sticky;
}
.hamburger{
  display: none;
  height: fit-content;
  cursor: pointer;
  padding: 3px 8px;
  border-radius: 5px;
  transition: 0.2s;
}
.hamburger:hover{
  background-color: grey;
}
.hamburger div {
  width:30px;
  height: 2px;
  margin: 6px 0;
  background: #212526;
}

/* .container {
  display: flex;
  justify-content: space-between;
  width: 100%;
  padding: 100px 100px 0  100px ;
} */

.logo-container{
  padding-left: 10rem;
  font-size: 50px;
  font-weight:900;
  font-family: Roboto, sans-serif;
  line-height: 1;
  display: flex;
  gap: 20px;
}
.logo-container p {
  color: black;
}
#logo{
  display: none;
}
#firstName {
  font-size: 50px;
}
#name{
  color: #0097b2;
}
@media screen and (max-width: 1500px) {
  .hamburger {
    display: block;
  }

  
  header {
    width: 90%;
    padding: 0 20px;
  }

  nav {
    padding-top: 5rem;
    position: absolute;
    left: -10%;
    top: 0;
    z-index: 999;
    width: 60%;
    height: 100vh;
    background: #fefefe;
    transition: transform 0.3s ease-in;
    box-shadow: 2px 0 20px 0 rgba(0,0,0,0);
    flex-direction: column;
    text-align: center;
    transform: translateX(-100%);
  }

  #nav_check:checked ~ nav {
    transform: translateX(0);
    box-shadow: 2px 0 20px 0 rgba(0,0,0,0.2);
  }

  .logo-container {
    font-size: 15px;
    padding: 0;
  }

  #firstName, #name {
    display: none;
  }

  #logo {
    display: block;
    height: 70px;
  }
}
@media screen and (max-width: 750px) {



  .hamburger {
    display: block;
  }
}
@media screen and (max-width: 500px) {
  .logo-container{
    font-size: 40px;
    
  }
  /* .container {
    padding: 50px;
  } */
  /* header{
    height: 8rem;
  } */
  
}
</style>
