<template>
  <div>
      <NavbarSection />
      <div class="container mt-4">
          <AboutSection />
          <ServicesSection />
          <AdvantageSection/>
          <ContactSection />
      </div>
      <footer>
          <p>&copy; 2024 PhagePlus</p>
      </footer>
  </div>
</template>

<script>
import NavbarSection from './components/NavbarSection.vue';
import AboutSection from './components/AboutSection.vue'; // Update the importimport Services from './components/Services-Company.vue';
import ContactSection from './components/ContactSection.vue';
import ServicesSection from './components/ServicesSection.vue';
import AdvantageSection from './components/AdvantageSection.vue';




export default {
  components: {
    NavbarSection,
      AboutSection, // Update the component registration
      ServicesSection,
      ContactSection,
      AdvantageSection,
  },
}
</script>
<style scoped>
/* styles.css */
.container {
  padding: 20px;
}

/* For mobile devices */
@media (max-width: 768px) {
  .container {
    padding: 10px;
  }
}

/* For larger screens */
@media (min-width: 769px) {
  .container {
    padding: 20px;
  }
}
</style>