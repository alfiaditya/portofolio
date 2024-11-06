<template>
<section class="relative w-full mt-20" id="contact" data-aos="zoom-in-up">
    <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg lg:max-w-screen-xl mx-auto relative">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div>
          <h1 class="pt-4 text-white font-bold text-2xl md:text-3xl lg:text-4xl">
            Let's Connect 👋
          </h1>
          <p class="text-gray-300 pt-8">
            I'm a recent graduate eager to apply my skills and knowledge in a challenging and rewarding environment. I'm particularly interested in web developer. Let's connect and discuss how I can contribute to your team.
          </p>
          <ul class="mt-8 text-left">
            <li class="mb-4">
              <i class="fas fa-envelope fa-lg  text-gray-300"></i> 
              <span class="text-primary">Email</span><br>
              <span class="text-white">alfiaditya12@gmail.com</span>
            </li>
            <li class="mb-4">
              <i class="fas fa-phone fa-lg  text-gray-300"></i> 
              <span class="text-primary">Phone</span><br>
              <span class="text-white">089663213582</span>
            </li>
            <li class="mb-4">
              <i class="fab fa-linkedin fa-lg  text-gray-300"></i> 
              <span class="text-primary">LinkedIn</span><br>
              <a href="https://www.linkedin.com/in/alfi-aditya-62047a1b8/" target="_blank" rel="noopener noreferrer" class="text-white">
                https://www.linkedin.com/in/alfi-aditya-62047a1b8/
              </a>
            </li>
          </ul>
        </div>
  
        <div class="bg-[#18224e] p-6 rounded-lg shadow-md">
          <h2 class="text-xl font-semibold text-white mb-4">Send Message</h2>
          <form @submit.prevent="sendEmail">
            <div class="mb-4">
              <label for="email" class="block text-gray-300 text-sm font-bold mb-2">Email</label>
              <input type="email" id="email" v-model="email" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
            </div>
            <div class="mb-4">
              <label for="subject" class="block text-gray-300 text-sm font-bold mb-2">Subject</label>
              <input type="text" id="subject" v-model="subject" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" required>
            </div>
            <div class="mb-4">
              <label for="message" class="block text-gray-300 text-sm font-bold mb-2">Message</label>
              <textarea id="message" v-model="message" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" rows="5" required></textarea>
            </div>
            <button type="submit" class="bg-orange-500 hover:bg-orange-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
  </template>
  <script>
  export default {
    data() {
      return {
        email: '',
        subject: '',
        message: ''
      }
    },
    methods: {
      sendEmail() {
        // Fungsi untuk mengirim email. 
        // Anda bisa menggunakan library email.js atau integrasi dengan backend API di sini.
        console.log('Email sent:', {
          email: this.email,
          subject: this.subject,
          message: this.message
        });
        // Reset form setelah email terkirim
        this.email = '';
        this.subject = '';
        this.message = '';
      }
    }
  }
  </script>