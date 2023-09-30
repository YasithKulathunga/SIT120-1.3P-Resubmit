<script>
import { RouterLink, RouterView } from 'vue-router'

function toggleMenu(){
  const menu = document.querySelector(".menu-links");
  const icon = document.querySelector(".menu-icon");
  menu.classList.toggle("open");
  icon.classList.toggle("open");
}
</script>

<template>
  <header>
    <nav id="desktop-nav">
        <div class="logo">hardydesigns</div>
        <div>
          <ul class="nav-links">
            <li><RouterLink class="router" to="/">Home</RouterLink></li>
            <li><RouterLink class="router" to="/about">Portfolio</RouterLink></li>
            <li><RouterLink class="router" to="/contact">Contact</RouterLink></li>
          </ul>
        </div>
      </nav>
      <nav id="mobile-nav">
        <div class="logo">hardydesigns</div>
        <div class="mobile-menu">
          <div class="menu-icon" onclick="toggleMenu()">
            <span></span>
            <span></span>
            <span></span>
          </div>
          <div class="menu-links">
            <li><RouterLink class="router" to="/" onclick="toggleMenu()">Home</RouterLink></li>
            <li><RouterLink class="router" to="/about" onclick="toggleMenu()">Portfolio</RouterLink></li>
            <li><RouterLink class="router" to="/contact" onclick="toggleMenu()">Contact</RouterLink></li>
          </div>
        </div>
      </nav>
  </header>
  <RouterView />
  <footer>
    <hr>
    <h2>All rights reserved</h2>
  </footer>
</template>

<style scoped>

hr{
  margin-top: 50px;
}

h2{
  text-align: center;
  margin: 30px;
}
header {
  line-height: 1.5;
  max-height: 100vh;
}

.router{
  text-decoration: none;
  color: black;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  
}

#desktop-nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

#mobile-nav{
  display: none;
}

.mobile-menu{
  position: relative;
  display: inline-block;
}

.menu-icon{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 24px;
  width: 30px;
  cursor: pointer;
}

.menu-icon span{
  width: 100%;
  height: 2px;
  background-color: black;
  transition: all 0.3 ease-in-out;
}

.menu-links{
  position:absolute;
  top: 100%;
  right: 0;
  background-color: white;
  width: fit-content;
  max-height: 0;
  overflow: hidden;
  transition: all 0.3 ease-in-out;
}

.menu-links a{
  display: block;
  padding: 10px;
  text-align: center;
  font-size: 1.5rem;
  color: black;
  text-decoration: none;
  transition: all 0.3 ease-in-out;
}

.menu-links li{
  list-style: none;
}

.menu-links.open{
  max-height: 300px;
}

.menu-icon.open span:first-child{
  transform: rotate(45deg) translate(10px 5px);
}
.menu-icon.open span:last-child{
  transform: rotate(-45deg) translate(10px -5px);
}
.menu-icon.open span:nth-child(2){
  opacity: 0;
}
.menu-icon.open span:first-child{
  transform: none;
}
.menu-icon.open span:first-child{
  opacity: 1;
}

.menu-icon.open span:first-child{
  transform: none;
}


@media screen and (max-width: 1200px) {
  #desktop-nav{
    display: none;
  }
  #mobile-nav{
    display: flex;
  }
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}



  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }

</style>
