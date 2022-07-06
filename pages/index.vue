<template>
  <div id="home" class="index">
    <Parallax/>
    <Header />
    <Home />
    <About />
    <HowTo />
    <Token />
    <RoadMap />
    <Faq />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/header/Header.vue';
import Home from '../components/page/Home.vue';
import About from '../components/page/About.vue';
import HowTo from '../components/page/HowTo.vue';
import Token from '../components/page/Token.vue';
import RoadMap from '../components/page/RoadMap.vue';
import Faq from '../components/page/Faq.vue';
import Contact from '../components/page/Contact.vue';
import Footer from '~/components/global/Footer.vue';
import Parallax from '~/components/global/Parallax.vue';
export default {
  name: "IndexPage",
  components: { Header, Home, About, HowTo, Token, RoadMap, Faq, Contact, Footer, Parallax },
  setup() {
    window.dataLayer = window.dataLayer || [];
    function gtag() { dataLayer.push(arguments); }
    gtag('js', new Date());

    gtag('config', 'G-ZT31KMBBXE');
  },
}
</script>

<style lang="scss" scoped>
.index {}
</style>
