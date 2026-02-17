<template>
  <div>
    <Header />
    <Hero />
    <About />
    <Services />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Services from './components/Services.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Header,
    Hero,
    About,
    Services,
    Contact,
    Footer
  }
}
</script>
