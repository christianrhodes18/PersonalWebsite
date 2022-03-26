<template>
    <div class="container">
        <form @submit.prevent="sendEmail">
            <label>Name</label>
            <input 
                type="text" 
                v-model="name"
                name="name"
                placeholder="Your Name"
            >
            <label>Email</label>
            <input 
                type="email" 
                v-model="email"
                name="email"
                placeholder="Your Email"
            >
            <label>Message</label>
            <textarea 
                name="message"
                v-model="message"
                cols="30" rows="5"
                placeholder="Message">
            </textarea>
            
            <input type="submit" value="Send">
        </form>

        <!-- Testing output -->
        <!-- <p>Name: {{ name }}</p>
        <p>Email: {{ email }}</p>
        <p>Message: {{ message }}</p> -->
    </div>

</template>

<script>
import emailjs from 'emailjs-com';
export default {
  name: 'ContactUs',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_r01upnr', 'template_ah4fh18', e.target, 'oPyYPxLyv1SPPn7Uu', {
          name: this.name,
          email: this.email,
          message: this.meessage
        })
      } catch (error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
}
</script>

<style>
/* .error {
    color: #ff0062;
    margin-top: 10px;
    font-size: 0.8em;
    font-weight: bold;
} */

* {
    box-sizing: border-box;
}
* form {
    max-width: 420px;
    margin: 20px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label {
    color: #aaa;
    display: inline-block;
    margin: 24px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input[type=text], [type=email], textarea, input {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
}
input[type=submit] {
    /* background-color: #4CAF50;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer; */

    background: #0b6dff;
    border: 0;
    padding: 10px 20px;
    margin-top: 20px;
    color: white;
    border-radius: 20px;
}
input[type=submit]:hover {
    background-color: #0058dd;
}
.container {
    display: block;
    margin: auto;
    text-align: center;
    border-radius: 8px;
    background-color: rgb(53, 48, 48);
    padding: 5px;
    width: 30%;
}
</style>