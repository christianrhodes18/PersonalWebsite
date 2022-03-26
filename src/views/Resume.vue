<template>
  <div class="resume">
    <h2>Resume</h2>
    <div class="container">
      <h3>Primary Skills</h3>
      <ul>
        <ul>Gameplay Programming - systems (quests, inventory, abilities), mechanics</ul>
        <ul>AI programming - behavior, combat</ul>
        <ul>Animation programming - adding custom animations and implementing them</ul>
        <ul>Game Design - level design, system design, combat design, cinematic design</ul>
      </ul>
      <h3>Secondary Skills</h3>
      <ul>
        <ul>Network programming</ul>
        <ul>Audio programming</ul>
        <ul>3D - Sculpting, modelling, texturing, animating, particles, lighting, compositing, rendering</ul>
      </ul>
      <h3>Software</h3>
      <ul>
        <ul>Unreal Engine</ul>
        <ul>Rider</ul>
        <ul>Blender</ul>
        <ul>Quixel Suite</ul>
        <ul>Source Control</ul>
      </ul>
    </div>
    <a id="download" href="https://drive.google.com/file/d/1BroM6SEiVah3v9ty2bY9zuZtx4j1WxSb/view?usp=sharing" title="resume_download" target="_blank">View Resume in Browser (Google Drive)</a>
    <div id="resume">
      <img id="resume-image" v-bind:src="resume" />
    </div>
  </div>
</template>

<script>
import resume from '../assets/resume.jpg'
export default {
  name: 'Resume',
  components: { },
  data: function() {
    return {
      resume: resume,
    }
  }
}
</script>

<style scoped>
.resume {
  font-family: 'Teko', sans-serif;
  font-size: 24px;
}
.resume h3 {
  /* display: inline-flex; */
  text-align: left;
  padding: 15px;
}
.container ul {
  /* display: inline-flex; */
  display: block;
  text-align: left;
  list-style-type: disc;
}
img {
  margin-top: 20px;
  max-width: 50%;
}
a {
  color: black;
  text-decoration: none;
}
a:hover {
  color: rgb(96, 106, 109);
  background-color: transparent;
  text-decoration: none;
}
a .resume-image {
  position: relative;
  text-align: center;
}

.container {
  margin-left: 20em;
  margin-right: 20em;
}

</style>