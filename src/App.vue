<template>
  <div class="bg-[#111827] min-h-screen">
    <Navbar />
    <HeroSection />
    <AboutSection />
    <SkillSection />
    <ProjectSection />
    <ContactSection />
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';
// import Component Asychronously
const Navbar = defineAsyncComponent(()=> import('@/components/NavBar.vue'))
const HeroSection = defineAsyncComponent(()=> import('@/components/HeroSection.vue'))
const AboutSection = defineAsyncComponent(()=> import('@/components/AboutSection.vue'))
const SkillSection = defineAsyncComponent(()=> import('@/components/SkillSection.vue'))
const ProjectSection = defineAsyncComponent(()=> import('@/components/ProjectSection.vue'))
const ContactSection = defineAsyncComponent(()=> import('@/components/ContactSection.vue'))

import { library } from '@fortawesome/fontawesome-svg-core'
import { faEnvelope, faPhone } from '@fortawesome/free-solid-svg-icons'
import { faInstagram, faLinkedin, faGithub } from '@fortawesome/free-brands-svg-icons'

library.add(faEnvelope, faPhone, faInstagram, faLinkedin, faGithub)
</script>
