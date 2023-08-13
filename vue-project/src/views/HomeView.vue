<script setup>
import Skip from '@/components/Skip.vue'
import Header from '@/components/Header.vue'
import Intro from '@/components/Intro.vue'
import Myinfo from '../components/Myinfo.vue'
import Skill from '@/components/Skill.vue'
import Site from '@/components/Site.vue'
import Port from '@/components/Port.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <div id="app">
    <!-- <Skip /> -->
    <Header />
    <main id="main" role="main">
      <Intro />
      <Skill />
      <Myinfo />
      <Site />
      <Port />
      <Contact />
    </main>
    <Footer />
  </div>
</template>
