<template>
  <Navigation />
  <div class="contact">
    <h2></h2>
    <p id="container">Feel free to send me a message. My email is thechristianrhodes@gmail.com , and this form will direct your message accordingly. Thank you for visiting my website! </p>
    <ContactForm/>
  </div>
</template>

<script>
import ContactForm from '../components/ContactForm.vue'
import Navigation from '../components/Navigation.vue'
export default {
  components: {
    ContactForm,
    Navigation,
  }
}
</script>

<style>
.contact h2 {
  margin-top: 80px;
}
.contact p {
  margin: 0 35% 50px 35%;
  text-align: left;
}

@media (max-width: 700px){
   .contact p {
    margin: 0 5% 50px 5%;
  }
}
</style>