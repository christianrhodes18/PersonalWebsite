<template>

  <!-- <div id="nav">
    <Navigation/>
  </div> -->

  <div id="content">
    <router-view/>
  </div>
  
  <div id="footer">
    <Footer/>
  </div>

</template>

<script>
import Navigation from './components/Navigation.vue'
import Footer from './components/Footer.vue'

export default {
  name: "App",
  components: {
    Navigation,
    Footer
  }
}
</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Teko:wght@300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed:ital,wght@0,300;1,700&family=Teko:wght@300&display=swap');

@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap');

html {
  /* background-color: rgba(237, 231, 217, 1); */
  background-color: #FBF9FF;
  width: 100%;
  height: 100%;
  min-height: 100vh;
}
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  /* font-family: 'Roboto Condensed', sans-serif; */
  /* font-family: 'Playfair Display', serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

h1 {
  font-size: 50px;
  font-style: bold;
  font-weight: 500;
}

h2 {
  font-size: 40px;
  font-weight: 300px;
}

p {
  font-size: 20px;
  text-align: left;
}

#nav {
  padding: 25px;
  padding-bottom: 40px;
  background-color: rgb(53, 48, 48);
}

#content {
  padding-bottom: 30px;
}

#footer {
  width: 100%;
  background-color: rgb(53, 48, 48)
}

@media (max-width: 500px){
   #footer {
     display: none;
   }
}

</style>
