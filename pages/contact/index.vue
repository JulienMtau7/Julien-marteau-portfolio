<template>
  <div class="contact">
    <h1>Contact me</h1>
    <form class="contact-form" @submit.prevent="sendEmail">
      <label>Name</label>
      <input
        type="text"
        name="name"
        placeholder="Your Name"
      >

      <label>Email</label>
      <input
        type="email"
        name="email"
        placeholder="Your Email"
        >

      <label>Message</label>
      <textarea
        name="message"
        cols="30" rows="5"
        placeholder="Message">
      </textarea>

      <input type="submit" value="Send">

      <div class="succesMsg">
        <p>Votre message a bien été envoyé !</p>
      </div>

      <div class="errorMsg">
        <p>Votre message a bien été envoyé !</p>
      </div>
    </form>
  </div>
</template>

<script>
  import emailjs from 'emailjs-com'

  export default {
    name:'Contact',

    methods: {
      sendEmail: (e) => {
        emailjs.sendForm('service_jc9rc07', 'template_2scokgv', e.target, 'user_ylL8Yr79oI6PVqJc3RKaL')
          .then((result) => {
              console.log('SUCCESS!', result.status, result.text);

              let succesMsg = document.querySelector('.succesMsg')
              succesMsg.classList.add('active')

          }, (error) => {
              console.log('FAILED...', error);
              let errorMsg = document.querySelector('.errorMsg')
              errorMsg.classList.add('active')
          });
      }
    }
  }
</script>

<style src="./contact.scss" lang="scss">

</style>
