<template>
  <div class="about">
    <h2>About</h2>
    <div class="container">
      <img v-bind:src="azsun">
      <p>Hello, I am Christian Rhodes and I am currently studying Computer Science at the University of Vermont. I am passionate about video games and how they are made. I have been programming since 2019 and participating in game development in various ways since 2021. My goal is to work in the AAA game industry contributing to the creation of modern games. I am always learning new techniques and industry practices to further my skills and propel me to work professionally in the industry after graduating university in 2023.</p>
    </div>
    <div>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis, corrupti? Dolores ad possimus, debitis quos non unde laboriosam libero odit vel, nobis corporis? Veniam velit ad magni libero? Aperiam itaque delectus et beatae aliquam? Vel modi suscipit tempora minus iste quisquam necessitatibus quibusdam alias. Deserunt placeat temporibus dicta laudantium alias sapiente. Sunt dignissimos doloremque illo, dolore molestias reprehenderit fugiat in hic dolorum suscipit amet atque incidunt, deserunt eligendi, laborum iste ratione. Asperiores aliquam eum harum nesciunt natus libero alias atque! Deleniti error dignissimos sapiente suscipit voluptatibus illum explicabo et exercitationem. Facere mollitia sapiente nihil est error perspiciatis voluptatum officiis iste.
      </p>
    </div>
  </div>
</template>

<script>
import azsun from '../assets/AZsun.jpg'
import image6 from '../assets/image6.jpg'
export default {
  name: 'About',
  components: { },
  data: function() {
    return {
      image6: image6,
      azsun: azsun,
    }
  }
}
</script>

<style scoped>
.container {
  column-count: 2;
  column-width: 14em;
  max-width: 1200px;
  display: block;
  text-align: left;
  margin-left: auto;
  margin-right: auto;
  margin: auto;
}
.container img {
  max-width: 70%;
  size: 50px;
  height: auto;
  padding-left: 10px;
}

p {
  font-size: 24px;
}

/* @media only screen and (min-width: 600px) {
  /* for tablets 
  
}

@media only screen and (min-width: 760px) {
  /* for desktop 
  
} */
</style>