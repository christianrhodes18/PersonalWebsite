<template>
    <div id="nav">
        <Navigation/>
    </div>

    <h2>Projects</h2>
    <div class="grid">
        <div class="grid-item">
            <h3>Unreal Engine 4 Feature Implementations</h3>
                    <img v-bind:src="UE4demo" />
                    <ul>
                        <ul><b>When: </b>Fall 2021</ul>
                        <ul><b>Project Scope: </b>Relatively small project to demonstrate basic front-end and back-end game mechanics</ul>
                        <ul><b>My Contributions: </b>Various game mechanics such as teleport, health bar, level loading, toggle 3rd/1st person, item inspect, AI, object spawner, and more</ul>
                        <ul><b>Engine and Tools: </b>Unreal Engine 4 using C++ and Blueprints</ul>
                        <ul><b>Project Link: </b><a href="https://youtu.be/BFA3xlDmVaQ" title="Uneral Engine 4 Game Mechanics Demo" target="_blank">YouTube Demo</a></ul>
                    </ul>
        </div>
        <div class="grid-item">
            <h3>C++ Bullet Hell Game</h3>
            <img v-bind:src="bullethellgif" />
            <ul>
                <ul><b>When: </b>May 2021</ul>
                <ul><b>Project Scope: </b>3 Level Bullet Hell with Story and Final Boss</ul>
                <ul><b>My Contributions: </b>2-person project. I programmed half the work, including graphics rendering, collision, HUD, level switch cases, etc.</ul>
                <ul><b>Engine and Tools: </b>C++, OpenGL, GLUT</ul>
                <ul><b>Project Link: </b><a href="https://github.com/christianrhodes18/Three-Level-Action-Game" title="C++ Bullet Hell GitHub Link" target="_blank">GitHub Project</a></ul>
            </ul>
        </div> 
        <div class="grid-item">
            <h3>Ongoing Game Jam 2022 Platformer</h3>
                    <img v-bind:src="fantasyplatformer" />
                    <ul>
                        <ul><b>When: </b>March 2022</ul>
                        <ul><b>Project Scope: </b>Initially for a 2-day game jam, expanding slightly</ul>
                        <ul><b>My Contributions: </b>Character, enemy, and weapon classes (including flipbook animations), managing animation notifies for 2D, level design and implementation. </ul>
                        <ul><b>Engine and Tools: </b>Unreal Engine 4 with Paper2D and PaperZD Plugin, Multi-User Editing in Unreal and Git for concurrent collaboration</ul>
                        <ul><b>Project Link: </b>Coming Soon</ul>
                    </ul>
        </div>
    </div>   
    
    <h2>More Projects related to 3D and Programming</h2>
    <div class="grid">
        <div class="grid-item">
            <h3>Blender Donut</h3>
            <img id="donut" v-bind:src="donut" />
            <ul>
                <ul><b>When: </b><span>January 2022</span></ul>
                <ul><b>Project Scope: </b>Create a complete model to practice 3D modelling and 3D art</ul>
                <ul><b>My Contributions: </b>All - modelling, sculpting, texturing, animation, particles, lighting, compositing, and rendering</ul>
                <ul><b>Engine and Tools: </b>Blender</ul>
                <ul><b>Project Link: </b><a href="https://www.artstation.com/artwork/lRzxA5" title="Blender Donut on ArtStation" target="_blank">Blender Donut on ArtStation</a></ul>
            </ul>
        </div>
        <div class="grid-item">
            <h3>Desert Environment using Unreal Engine 5</h3>
            <img v-bind:src="desert" />
            <ul>
                <ul><b>When: </b>November, 2021</ul>
                <ul><b>Project Scope: </b>Short cinematic showcasing UE5 graphics</ul>
                <ul><b>My Contributions: </b>Enviornment design, animating mannequins, post-processing</ul>
                <ul><b>Engine and Tools: </b>Unreal Engine 5, Quixel Megascans, DaVince Resolve</ul>
                <ul><b>Project Link: </b><a href="https://www.artstation.com/artwork/8w5qYx" title="Desert Environment on ArtStation" target="_blank">Desert Enviornment on ArtStation</a></ul>
            </ul>
        </div>
        <div class="grid-item">
            <h3>This Website!</h3>
            <img v-bind:src="vuecode" />
            <ul>
                <ul><b>When: </b>February-March 2022</ul>
                <ul><b>Project Scope: </b>Portfolio Site with a few pages to highlight personal experience and skill. Adding content as I complete projects.</ul>
                <ul><b>My Contributions: </b>All. Component-based workflow, SPA rendering</ul>
                <ul><b>Engine and Tools: </b>HTML, CSS, JS, Vue.js, VSCode</ul>
            </ul>
        </div>
    </div>
</template>

<script>
import Navigation from '../components/Navigation.vue'

import image4 from '../assets/image4.jpg'
import image1 from '../assets/image1.jpg'
import image2 from '../assets/image2.jpg'
import image5 from '../assets/image5.jpg'

import UE4demo from '../assets/UE4GameMechanics.gif'
import bullethellgif from '../assets/bullethell.gif'
import fantasyplatformer from '../assets/fantasyplatformer.gif'
import donut from '../assets/blenderdonut.gif'
import desert from '../assets/desert.gif'
import vuecode from '../assets/vuegif.gif'
export default {
  name: 'Portfolio',
  components: {
        Navigation
    },
  data: function() {
    return {
      image4: image4,
      image1: image1,
      image2: image2,
      image5: image5,
      UE4demo: UE4demo,
      bullethellgif: bullethellgif,
      fantasyplatformer: fantasyplatformer,
      donut: donut,
      desert: desert,
      vuecode: vuecode,
    }
  }
}
</script>

<style scoped>
.portfolio {
    margin-bottom: 120px;
}

/* * {
  box-sizing: border-box;
}  */


ul {
    text-align: left;
    padding-top: 3px;
}

a {
    text-decoration: none;
}

hr {
    display: block;
    height: 3px;
    border: 0;
    border-top: 1px solid #ccc;
    margin: 1em 0;
    padding: 0;
}

#donut {
    width: 50%;
} 

img {
  margin-top: 20px;
  max-width: 90%;
}


.grid{
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 1fr;
  column-gap: 20px;
  padding: 20px;
  margin-left: auto;
  margin-right: auto;
}

.grid-item {
    background-color: rgba(73, 37, 70, 0.212);
}

@media (max-width: 900px){
   .grid{
      grid-template-columns: repeat(1, 1fr);
   }
}
</style>