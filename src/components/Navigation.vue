<template>
  <header id="nameBar">
      <h1 id="name">Christian Rhodes</h1>
      <!-- <h2 id="profession">Gameplay Programmer and Software Developer</h2> -->
  </header>
  <hr/>
  <body>
      <nav class="navMenu">
        <a><router-link class="link" :to="{ name: 'Home' }">Home</router-link></a>
        <!-- <a><router-link class="link" :to="{ name: 'Portfolio' }">Portfolio</router-link></a>
        <a><router-link class="link" :to="{ name: 'Resume' }">Resume</router-link></a>
        <a><router-link class="link" :to="{ name: 'About' }">About</router-link></a>
        <a><router-link class="link" :to="{ name: 'Contact' }">Contact</router-link></a> -->
        <div class="dot"></div>
      </nav>
  </body>
</template>

<script>
export default {
    name: "navigation",
    data() {
        return {
            scrolledNav: null,
            mobile: null,
            mobileNav: null,
            windowWidth: null,
        }
    }
}
</script>

<style lang="scss" scoped>

/* nameBar */
#nameBar {
  /* display: grid;
  grid-template-columns: 50% 50%;
  /* grid-template-columns: 35% 65%; */
  /* grid-template-rows: 1fr; */
  max-height: 100px;
}
#nameBar #name {
  font-size: 50px;
}
#nameBar #profession {
  font-size: 50px;
}
header {
    /* color: #FBF9FF; */
    color: #000000;
    text-align: center;
    font-style: bold;
}

/* bar */
hr {
    display: block;
    height: 3px;
    border: 0;
    border-top: 1px solid #ccc;
    margin: 1em 0;
    padding: 0;
}

/* nav menu */
nav a:hover,
nav a.router-link-active,
nav a.router-link-exact-active {
  color: rgba(145, 166, 255, 1);
  
}
body {
  font-size: 14px;
}
.navMenu {
  position: absolute;
  margin-top: 20px;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}
.navMenu a {
  /* color: rgb(255, 255, 255); */
  color: black;
  text-decoration: none;
  font-size: 1.2em;
  text-transform: uppercase;
  font-weight: 500;
  display: inline-block;
  width: 80px;
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

/* navMenu dot animations */
.navMenu .dot {
  width: 6px;
  height: 6px;
  background: rgba(145, 166, 255, 1);
  border-radius: 50%;
  opacity: 0;
  -webkit-transform: translateX(30px);
  transform: translateX(30px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}
.navMenu a:nth-child(1):hover ~ .dot {
  -webkit-transform: translateX(38px);
  transform: translateX(38px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}
.navMenu a:nth-child(2):hover ~ .dot {
  -webkit-transform: translateX(120px);
  transform: translateX(120px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}
.navMenu a:nth-child(3):hover ~ .dot {
  -webkit-transform: translateX(195px);
  transform: translateX(195px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}
.navMenu a:nth-child(4):hover ~ .dot {
  -webkit-transform: translateX(280px);
  transform: translateX(280px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}
.navMenu a:nth-child(5):hover ~ .dot {
  -webkit-transform: translateX(360px);
  transform: translateX(360px);
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  opacity: 1;
}



/* RESPONSIVE */
@media (max-width: 900px){
   #nameBar {
      grid-template-columns: repeat(1, 1fr);
   }
}
</style>