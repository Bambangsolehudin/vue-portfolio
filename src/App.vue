<template>
  <div id="app">
    <!-- ======= Header ======= -->
    <header id="header">
      <div class="container">
        <Home />
      </div>
    </header><!-- End Header -->

    <!-- ======= About Section ======= -->
    <section id="about" class="about">
      <About />
    </section><!-- End About Section -->

    <!-- ======= Resume Section ======= -->
    <section id="resume" class="resume">
      <Resume />
    </section><!-- End Resume Section -->

   

    <!-- ======= Portfolio Section ======= -->
    <section id="portfolio" class="portfolio">
      <Portfolio />
    </section><!-- End Portfolio Section -->

    <!-- ======= Contact Section ======= -->
    <section id="contact" class="contact">
     <Contact />
    </section><!-- End Contact Section -->

    <div class="credits">
      Portfolio Bambang Solehudin
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Home from './components/Portfolio/Home.vue'
import About from './components/Portfolio/About.vue'
import Resume from './components/Portfolio/Resume.vue'
import Contact from './components/Portfolio/Contact.vue'
import Portfolio from './components/Portfolio/Portfolio.vue'







export default {
  name: 'App',
  components: {
    // HelloWorld
    Home,
    About,
    Resume,
    Contact,
    Portfolio
  },
  mounted () {
    var scripts = [
      "template/assets/vendor/purecounter/purecounter_vanilla.js",
      "template/assets/vendor/bootstrap/js/bootstrap.bundle.min.js",
      "template/assets/vendor/glightbox/js/glightbox.min.js",
      "template/assets/vendor/isotope-layout/isotope.pkgd.min.js",
      "template/assets/vendor/swiper/swiper-bundle.min.js",
      "template/assets/vendor/waypoints/noframework.waypoints.js",
      "template/assets/vendor/php-email-form/validate.js",
      "template/assets/js/main.js"

    ];
    scripts.forEach(script => {
      let tag = document.createElement("script");
      tag.setAttribute("src", script);
      document.head.appendChild(tag);
    });
  },
}
</script>

<style>
    @import '../public/template/assets/vendor/bootstrap/css/bootstrap.min.css';
    @import '../public/template/assets/vendor/bootstrap-icons/bootstrap-icons.css';
    @import '../public/template/assets/vendor/boxicons/css/boxicons.min.css';
    @import '../public/template/assets/vendor/glightbox/css/glightbox.min.css';
    @import '../public/template/assets/vendor/remixicon/remixicon.css';
    @import '../public/template/assets/vendor/swiper/swiper-bundle.min.css';
    @import '../public/template/assets/css/style.css';

    


 


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
