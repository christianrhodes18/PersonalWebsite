<template>
  <!-- LANDING PAGE -->
	<section class="showcase" id="home">
			<div class="video-container">
        <img v-bind:src="rockydesert" alt="Landing Page BG Image"/>
				<!-- <video src="https://traversymedia.com/downloads/video.mov" autoplay muted loop></video> -->
			</div>

			<div class="content">
				<h1>Christian <span>Rhodes</span></h1>
				<h3>Game Programmer <span>+</span> Software Developer</h3>
        <!-- <a href="#about" class="btn">About Me</a> -->
        
        <h2 class="above-arrow">About</h2>
        <br>
        <a href="#about" class="arrow"><img v-bind:src="arrow" /></a>
      
        <!-- BUTTONS TO REDIRECT TO WEB PAGES (UNUSED) -->
        <!-- <div class="button-container">
          <div class="button" id="button-2">
            <div id="slide"></div>
            <a><router-link class="link" :to="{ name: 'Portfolio' }">Portfolio</router-link></a>
          </div>
          <div class="button" id="button-2">
            <div id="slide"></div>
            <a><router-link class="link" :to="{ name: 'Resume' }">Resume</router-link></a>
          </div>
        </div>
        <div class="button-container">
          <div class="button" id="button-2">
            <div id="slide"></div>
            <a><router-link class="link" :to="{ name: 'Contact' }">Contact</router-link></a> 
            <a href="#about" >About</a>
          </div>
        </div> -->
			</div>
  </section>

  <!-- ABOUT SECTION -->
  <section id="about">      
    <div class="columnsContainer">
      <div class="leftColumn">
        <!-- <h2>Left Column (fluid)</h2> -->
        <h1>About Me</h1>
        <p>
        Hello, I am Christian Rhodes and I'm 23 years old. I am currently studying Computer Science at the University of Vermont. 
        I am passionate about video games and how they are made! I have been programming since 2019 and participating 
        in game development in various ways since 2021. My goal is to work in the AAA game industry contributing to the 
        creation of modern game experiences. I am always learning new techniques and industry practices to further my skills and 
        propel me to work professionally in the industry after graduating university in 2023.
        </p>
        <div class="divider div-transparent div-arrow-down"></div>

        <!-- SKILLS SECTION -->
        <h2>My Skills</h2>
        <div class="interest">
          <div class="grid-skills">
            <div class="grid-item">
              <h3>Game Development</h3>
              <img id="gifs" v-bind:src="fantasyplatformer" />
              <div class="item-description">
                <ul>
                  <h4>Gameplay Programming</h4>
                  <li>Systems (Quests, Inventory, Abilities)</li>
                  <li>Mechanics</li>
                  <li>AI (Behavior, Combat)</li>
                  <li>Animation</li>
                  <h4>Game Design</h4>
                  <li>Level design</li>
                  <li>System design</li>
                  <li>Combat design</li>
                  <li>Cinematic design</li>
                </ul>
              </div>   
            </div>

            <div class="grid-item">
              <h3>Coding</h3>
              <img id="gifs" v-bind:src="vuecode" />
              <div class="item-description">
                <ul>
                  <h4>Languages (by familiarity)</h4>
                  <li><b>C++</b> (since 2020)</li>
                  <li><b>Python</b> (since 2019)</li>
                  <li><b>C#</b> (since 2020)</li>
                  <li><b>HTML, CSS, Javascript</b> (since 2019)</li>
                  <li><b>C</b> (since 2022)</li>
                  <h4>Applications</h4>
                  <li>Game Programming</li>
                  <li>Misc. Projects</li>
                  <li>Web Development (full stack)</li>
                </ul>
              </div>   

            </div> 
            <div class="grid-item">
              <h3>3D / Environments</h3>
              <img id="gifs" v-bind:src="desert" />
              <div class="item-description">
                <ul>
                <h4>3D</h4>
                  <li>Modelling and Sculpting</li>
                  <li>Texturing</li>
                  <li>Animation</li>
                  <li>Lighting and Particles</li>
                  <li>Compositing and Rendering</li>
                <h4>3D Creations</h4>
                  <li>Realistic / Stylized Environments</li>
                  <li>Characters</li>
                  <li>Objects</li>
                  <li>Cinematic Shorts</li>
                </ul>
              </div>   
            </div> 
          </div>
        </div>
      </div>

      <!-- RIGHT SIDE PHOTOS -->
      <div class="rightColumn">
        <img id="portrait" v-bind:src="azsun" alt="Portrait Image">
        <img id="mountain-photo" v-bind:src="mountains" alt="Mountains Image">
      </div>

    </div>

    <!-- PORTFOLIO SECTION -->
    <div id="portfolio">
      <div class="divider div-transparent div-arrow-down"></div>
      <h2>View Portfolio</h2>
      
      <!-- Dynamic Button Text -->
      <a v-if="showPortfolio" class="btn2" v-on:click="togglePortfolio()">{{ contentShownText }}</a>
      <a v-if="!showPortfolio" class="btn2" v-on:click="togglePortfolio()">{{ contentHiddenText }}</a>

      <!-- Show Portfolio on click -->
      <div v-if="showPortfolio">
        <div id="toggle-space">
          <h2>Projects</h2>
        </div>
        <div class="grid-portfolio">
          <div class="grid-item">
              <h3>Unreal Engine 4 Feature Implementations</h3>
              <img v-bind:src="UE4demo" />
              <ul class="item-description">
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
              <ul class="item-description">
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
              <ul class="item-description">
                  <ul><b>When: </b>March 2022</ul>
                  <ul><b>Project Scope: </b>Initially for a 2-day game jam, expanding slightly</ul>
                  <ul><b>My Contributions: </b>Character, enemy, and weapon classes (including flipbook animations), managing animation notifies for 2D, level design and implementation. </ul>
                  <ul><b>Engine and Tools: </b>Unreal Engine 4 with Paper2D and PaperZD Plugin, Multi-User Editing in Unreal and Git for concurrent collaboration</ul>
                  <ul><b>Project Link: </b>Coming Soon</ul>
              </ul>
          </div>
        </div>
        <div id="toggle-space">
          <h2>More Projects related to 3D and Programming</h2>
        </div>
        <div class="grid-portfolio">
            <div class="grid-item">
              <h3>Blender Donut</h3>
              <img id="donut" v-bind:src="donut" />
              <ul class="item-description">
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
              <ul class="item-description">
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
              <ul class="item-description">
                <ul><b>When: </b>February-March 2022</ul>
                <ul><b>Project Scope: </b>Portfolio Site with a few pages to highlight personal experience and skill. Adding content as I complete projects.</ul>
                <ul><b>My Contributions: </b>All. Component-based workflow, SPA rendering</ul>
                <ul><b>Engine and Tools: </b>HTML, CSS, JS, Vue.js, VSCode</ul>
              </ul>
            </div>
          </div>

      <a class="btn2" v-on:click="togglePortfolio()">{{ contentShownText }}</a>

      </div>
    </div>


    <!-- RESUME SECTION -->
    <div id="resume">
      <div class="divider div-transparent div-arrow-down"></div>
      <h2>View Resume</h2>

      <!-- Dynamic Button Text -->
      <a v-if="showResume" class="btn2" v-on:click="toggleResume()">{{ contentShownText }}</a>
      <a v-if="!showResume" class="btn2" v-on:click="toggleResume()">{{ contentHiddenText }}</a>

      <!-- Show Resume on click -->
      <div v-if="showResume">

        <!-- SOCIALS (PROFESSIONAL) -->
        <div id="toggle-space">
          <h2><u>Professional Socials</u></h2>
        </div>
        <div class="social">
          <!-- <h2>Follow Me On Social Media</h2> -->
          <!-- <a href="https://github.com/christianrhodes18" title="Github" target="_blank"><i class="fa fa-2x fa-github"></i></a>
          <a href="https://www.linkedin.com/in/christianrhodes18/" title="Linkedin" target="_blank"><i class="fa fa-2x fa-linkedin"></i></a> -->
          <!-- <a href="https://twitter.com/chrisrhodesy" title="Twitter" target="_blank"><i class="fa fa-2x fa-twitter"></i></a> -->
          <div class="grid-socials">
            <p>You can find some of my coding projects on my GitHub, like video game 
              source code and code projects featuring various programming languages and applications. </p>
            <div class="grid-item">
              <a href="https://github.com/christianrhodes18" title="GitHub" target="_blank" id="custom-logo"><img v-bind:src="github_logo"></a>
            </div>
            <br>
            <p>My Linkedin contains professional materials, connections, and contact information. </p>
            <div class="grid-item">
              <a href="https://www.linkedin.com/in/christianrhodes18/" title="Linkedin" target="_blank" id="custom-logo"><img v-bind:src="linkedin_logo"></a>
            </div>
            <br>
            <p>My artstation features some of my 3D work, like 3D models and environments. </p>
            <br>
            <div class="grid-item">
              <a href="https://www.artstation.com/takensoulz" title="Artstation" target="_blank" id="custom-logo"><img v-bind:src="artstation_logo"></a>
            </div>
          </div>
        </div>

        <!-- SOFTWARE -->
        <div id="toggle-space">
          <h2><u>Software</u></h2>
        </div>
        <div class="grid-software">
          <div class="grid-item">
            <img v-bind:src="ue_logo" alt="Unreal Engine">
            <!-- <p>Since 2021</p> -->
          </div>
          <div class="grid-item">
            <img v-bind:src="rider_logo" alt="JetBrains Rider">
            <!-- <p>Since 2022</p> -->
          </div>
          <div class="grid-item">
            <img v-bind:src="unity_logo" alt="Unity">
            <!-- <p>Since 2020</p> -->
          </div>
          <div class="grid-item">
            <img v-bind:src="blender_logo" alt="Blender">
            <!-- <p>Since 2021</p> -->
          </div>
          <div class="grid-item">
            <img v-bind:src="quixel_logo" alt="Quixel Suite">
            <!-- <p>Since 2021</p> -->
          </div>
          <div class="grid-item">
            <img v-bind:src="git_logo" alt="Git">
            <!-- <p>Since 2019</p> -->
          </div>
        </div>

        <!-- RESUME PDF LINK -->
        <div class="resume-link" id="toggle-space">
          <h2><u>My Resume</u></h2>
          <a id="download" href="https://drive.google.com/file/d/1TUWHh7Na-cqPj0CGrPstkSQHs6jg1LFE/view?usp=sharing" title="resume_download" target="_blank">View Resume in Browser (Google Drive)</a>
        </div>
        <div id="toggle-space-lower">
          <h3></h3>
        </div>
        <a class="btn2" v-on:click="toggleResume()">{{ contentShownText }}</a>
      </div>
    </div>


    <!-- FOLLOW THEN FOOTER -->
    <div class="divider div-transparent div-stopper"></div>
    <div class="social">
      <!-- <h2>Contact Me</h2> -->
      <div id="toggle-space">
        <h2></h2>
      </div>
      <a><router-link class="link" :to="{ name: 'Contact' }"><h2>Contact Me Here</h2></router-link></a> 
      <div class="divider div-transparent"></div>
    </div>
  </section>
  <a href="#home" class="btn2">Back to Top</a>
</template>




<script>
// IMPORTS
import azsun from '../assets/AZsun.jpg'
import arrow from '../assets/downarrow.png'
import profilepicture from '../assets/2019_ProfPic.jpg'
import rockydesert from '../assets/rockydesert2.png'
import gameicon from '../assets/icons8-game-96-backup.png'
import fantasyplatformer from '../assets/fantasyplatformer.gif'
import vuecode from '../assets/vuegif.gif'
import desert from '../assets/desert.gif'
import mountains from '../assets/mountainview.jpg'

// PORTFOLIO IMPORTS
import UE4demo from '../assets/UE4GameMechanics.gif'
import bullethellgif from '../assets/bullethell.gif'
import donut from '../assets/blender-donut.gif'

// RESUME IMPORTS
import blender_logo from '../assets/blender_logo.png'
import ue_logo from '../assets/ue_logo.png'
import rider_logo from '../assets/rider_logo.png'
import quixel_logo from '../assets/quixel_logo.png'
import git_logo from '../assets/git_logo.png'
import unity_logo from '../assets/unity_logo.png'
import artstation_logo from '../assets/artstation_logo.png'
import github_logo from '../assets/github_logo.png'
import linkedin_logo from '../assets/linkedin_logo.png'

export default {
  name: 'Home',
  components: {},
  data: function() {
    return {
      azsun: azsun,
      arrow: arrow,
      profilepicture: profilepicture,
      rockydesert: rockydesert,
      gameicon: gameicon,
      fantasyplatformer: fantasyplatformer,
      vuecode: vuecode,
      desert: desert,
      mountains: mountains,
      showPortfolio: false,
      showResume: false,
      UE4demo: UE4demo,
      bullethellgif: bullethellgif,
      donut: donut,
      contentHiddenText: 'Show',
      contentShownText: 'Hide',
      blender_logo: blender_logo,
      ue_logo: ue_logo,
      rider_logo: rider_logo,
      quixel_logo: quixel_logo,
      git_logo: git_logo,
      unity_logo: unity_logo,
      artstation_logo: artstation_logo,
      github_logo: github_logo,
      linkedin_logo: linkedin_logo,
    }
  },
  methods: {
    // toggles portfolio section with v-on:click event
    togglePortfolio() {
      this.showPortfolio = !this.showPortfolio
      //console.log(this.showPortfolio)
    },
    // toggles resume section with v-on:click event
    toggleResume() {
      this.showResume = !this.showResume
      //console.log(this.showResume)
    }
  },
}
</script>




<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400&display=swap');
@import url("//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css");

/* GENERAL PROPERTIES */
* {
	box-sizing: border-box;
	padding: 0;
}
body {
	font-family: 'Open Sans', sans-serif;
	line-height: 1.5;
}
a {
	text-decoration: none;
	color: var(--primary-color);
}
h1 {
/* 	font-weight: 300; */
/* line-height: 1.2; */
	font-size: 60px;
	margin-bottom: 15px;
}
h4 {
  font-size: 18px;
  margin: 5px 0 5px 0;
}




/* LANDING PAGE SECTION */
.showcase {
  font-family: 'Playfair Display', serif;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
	text-align: center;
	color: #fff;
	padding: 0 20px;
}
.video-container {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	overflow: hidden;
	/* background: var(--primary-color) url('./https://traversymedia.com/downloads/cover.jpg') no-repeat center
		center/cover; */
}
/* change to video when added */
.video-container img {
	min-width: 100%;
	min-height: 100%;
  position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	object-fit: cover;
}
.video-container:after {
	content: '';
	z-index: 1;
	height: 100%;
	width: 100%;
	top: 0;
	left: 0;
	background: rgba(0, 0, 0, 0.3);
	position: absolute;
}
.content {
	z-index: 2;
}



/* BUTTON - REUSED A COUPLE TIMES */
.btn {
	display: inline-block;
	padding: 10px 30px;
  background: rgba(0, 0, 0, 0.5);
	color: #fff;
	border-radius: 5px;
	border: solid #fff 1px;
	margin-top: 25px;
	opacity: 0.85;
}
.btn:hover {
	transform: scale(0.98);
}
.btn2 {
	display: inline-block;
	padding: 15px 25px;
  background: rgba(0, 0, 0, 0.5);
	color: #fff;
	border-radius: 5px;
	border: solid #fff 1px;
	opacity: 0.85;
}
.btn2:hover {
	transform: scale(0.98);
  cursor: pointer;
}
h2.above-arrow {
  position: absolute;
  margin-bottom: -10px;
  top: 82%;
  left: 40%;
  right: 40%;
  font-size: 30px;
}
.arrow:hover {
  cursor:auto;
}
.arrow img{
  display: inline-block;
  /* position: absolute; */
  /* margin: 20% 0 0 -6%; */
  margin-bottom: -300px;
  max-height: 50px;
  background-color: rgba(255, 255, 255, .1);
}
.arrow img:hover {
  cursor: pointer;
  transform: scale(.5);
  transform: translate(0, 2.5px);
}




/* ABOUT SECTION */
#about {
	padding: 0 40px 40px 40px;
	text-align: center;
}
#about p {
	font-size: 1.2rem;
	max-width: 600px;
	margin: auto;
}
#about h2 {
	margin: 30px 0;
	color: var(--primary-color);
}
#about h3 {
	color: var(--primary-color);
  font-size: 24px;
  background-image: linear-gradient(to right, rgba(0,0,0,0), rgba(181,209,248, .3));
  border-radius: 7px;
}



/* DIVIDERS */
.divider
{
	position: relative;
	margin-top: 40px;
	height: 1px;
}
.div-transparent:before
{
	content: "";
	position: absolute;
	top: 0;
	left: 5%;
	right: 5%;
	width: 90%;
	height: 1px;
	background-image: linear-gradient(to right, transparent, rgb(48,49,51), transparent);
}
.div-arrow-down:after
{
	content: "";
	position: absolute;
	z-index: 1;
	top: -7px;
	left: calc(50% - 7px);
	width: 14px;
	height: 14px;
	transform: rotate(45deg);
	background-color: white;
	border-bottom: 1px solid rgb(48,49,51);
	border-right: 1px solid rgb(48,49,51);
}
.div-stopper:after
{
	content: "";
	position: absolute;
	z-index: 1;
	top: -6px;
	left: calc(50% - 7px);
	width: 14px;
	height: 12px;
	background-color: white;
	border-left: 1px solid rgb(48,49,51);
	border-right: 1px solid rgb(48,49,51);
}







/* Buttons */
#button-container {
  width: 100%;
  margin: 0 auto;
  padding: 50px 0 150px 0;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.button {
  display: inline-flex;
  height: 40px;
  width: 150px;
  border: 2px solid #BFC0C0;
  margin: 20px 20px 20px 20px;
  color: #BFC0C0;
  text-transform: uppercase;
  text-decoration: none;
  font-size: 1.2em;
  letter-spacing: 1.5px;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  background: rgba(255, 255, 255, 0.1);
}
#button-2 {
  position: relative;
  overflow: hidden;
  cursor: pointer;
}
#button-2 a {
  position: relative;
  transition: all .35s ease-Out;
}
#slide {
  width: 100%;
  height: 100%;
  left: -200px;
  background: #BFC0C0;
  position: absolute;
  transition: all .35s ease-Out;
  bottom: 0;
}
#button-2:hover #slide {
  left: 0;
}
#button-2:hover a {
  color: #2D3142;
} 



/* SKILLS SECTION */
.item-description {
  text-align: left;
}
.item-description ul {
  padding-left: 15px;
  list-style-type: none;
}
.item-description li {
  padding-left: 20px;
}
#gifs {
  max-width: 100%;
  max-height: 200px;
}



/* RIGHT SIDE IMAGES */
#portrait {
  max-width: 100%;
  max-height: 800px;
  border-radius: 8px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
#mountain-photo {
  margin: 80px 0 5px 0;
  max-width: 100%;
  max-height: 350px;
  border-radius: 8px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.25);
  display: none;
}



/* TWO COLUMN SECTION FROM ABOUT TO PORTFOLIO */
body {
  margin: 0;
}
.columnsContainer, footer, header {
  position: relative;
  margin: .5em;
}
.leftColumn, .rightColumn, footer, header {
  /*border: 1px solid  #ccc;*/
  padding: 1.25em;
} 
.leftColumn {
  margin-bottom: .5em;
}
.inline-items {
  margin-top: 0;
}
.inline-items li {
  margin-left: 0;
  border-left: 1px solid black;
  padding-left: 10px;
  padding-right: 10px;
}
.inline-items li:first-child {
  margin-left: 0;
  border: none;
  padding-left: 0;
  padding-right: 10px;
}
.inline-items li:last-child {
  padding-right: 0;
}



/* GRID LAYOUTS (GIFS, PROJECTS) */
.grid-skills {
  display: grid;
  grid-template-columns: auto auto auto;
  /* grid-template-columns: 50% 50%; */
  grid-template-rows: 1fr;
  column-gap: 20px;
  margin-top: -20px;
  margin-left: auto;
  margin-right: auto;
}
.grid-portfolio {
  display: grid;
  /* grid-template-columns: 33.33% 33.33% 33.33%; */
  grid-template-columns: auto auto auto;
  /* grid-template-columns: 50% 50%; */
  grid-template-rows: 1fr;
  column-gap: 20px;
  margin-top: -20px;
  margin-left: auto;
  margin-right: auto;
}
.grid-portfolio img {
  max-width: 100%;
}
.grid-portfolio a {
  color: blue;
}
.grid-portfolio #donut {
  max-height: 350px;
}
.grid-software {
  display: grid;
  grid-template-columns: auto auto auto auto auto auto;
  /* grid-template-columns: 50% 50%; */
  grid-template-rows: 1fr;
  column-gap: 20px;
  margin-top: 30px;
  margin-left: auto;
  margin-right: auto;
}
.grid-software img {
  max-width: 100px;
  max-height: 80px;
}
.grid-software p {
  text-align: center;
  margin-top: 15px;
}
.grid-socials {
  display: grid;
  grid-template-columns: auto auto auto;
  /* grid-template-columns: 50% 50%; */
  grid-template-rows: 1fr;
  column-gap: 20px;
  margin-top: -20px;
  margin-left: auto;
  margin-right: auto;
}
.grid-socials img {
  max-width: 200px;
  max-height: 80px;
}
/* .grid-item {
    background-color: rgba(73, 37, 70, 0.212);
} */
#toggle-space a {
  color: blue;
  margin-bottom: 20px;
}
#toggle-space h2 {
  margin: 50px 0 50px 0;
}
#toggle-space-lower h3 {
  margin-bottom: 30px;
}



/* PORTFOLIO SPECIFIC */
/* #portfolio {
  background-color: rgba(199, 238, 207, 0.26);
} */




/* RESUME SPECIFIC */
/* #resume {
  background-color: rgba(210, 238, 255, 0.267);
} */




/* SOCIAL SECTION AT BOTTOM */
.social {
  position: relative;
  /* height: 50px; */
}
.social .fa {
	/* margin: 30px 10px 30px 10px; */ /*top, right, bottom, left*/
  padding: 20px;
  /* max-height: 300px; */
  /* margin-top: 10em; */
}
.social #custom-logo img {
  max-height: 100px;
}
.social a {
  color: rgb(0, 0, 34);
  text-decoration: underline;
}
.social p {
  margin: auto auto;
}




/* MEDIA QUERIES */
/* For largest size */
@media screen and (min-width: 1285px ) { /*37.5em*/
  .leftColumn {
    margin-right: 29.5em;
    }

	.rightColumn {
    position: absolute; top: 0; right: 0; width: 28.75em;
    }
  #portrait {
    margin-top: 80px;
  }
  #mountain-photo {
     display: inline;
  }
  #portrait {
    max-width: 100%;
    height: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  }
}
/* Stack skills section */
@media (max-width: 980px){
   .grid-skills {
      grid-template-columns: repeat(1, 1fr);
   }
   .grid-portfolio {
      grid-template-columns: repeat(1, 1fr);
   }
   .grid-socials {
      grid-template-columns: repeat(1, 1fr);
   }
   .grid-socials img {
      max-width: auto;
   }
   .grid-software {
      grid-template-columns: repeat(3, 1fr);
   }
   #about h3 {
     font-size: 30px;
   }
   .item-description h4 {
     text-align: center;
     font-size: 24px;
     margin: 20px 0 10px 0;
    }
   .item-description li {
     margin: 0 0 0 0;
     padding: 0 0 0 0;
     text-align: left;
     font-size: 18px;
    }
   .leftColumn, .rightColumn, footer, header {
    /*border: 1px solid  #ccc;*/
    padding: 0;
    } 
   #gifs {
     max-height: 500px;
     max-width: 100%;
    }
   #portrait {
    max-height: 600px;
    }
}
/* Extra Rules exclusive to Mobile */
@media (max-width: 550px){
  .grid-software {
      grid-template-columns: repeat(2, 1fr);
   }
  .grid-software img {
      margin-bottom: 40px;
   }
   .video-container img {
    transform: translate(-55%, -50%);
  }
  .arrow img{
    margin-bottom: -250px;
  }
  .showcase h1 span {
    display: block;
  }
  .showcase h3 span {
    display: block;
  }
}
</style>
