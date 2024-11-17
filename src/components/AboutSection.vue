<template>
    <section id="about" class="mb-5">
        <h2>About Us</h2>
        <p>
            At PhagePlus, we work on sterilizing water in a sustainable and natural way that rids water of harmful bacteria in water sources in an innovative way using genetically modified bacteriophages.
        </p> 
          
        <p>Mechanism of action: Bacteriophages are developed that are able to bind to harmful bacteria and reproduce inside them to destroy them. They can be designed in a laboratory with precise design according to the bacteria present in the water. PhagePlus can be used in water treatment plants, water tanks, etc., as after receiving a sample of that water, the bacterial pollutants present in it can be identified, then phages or bacteriophages designed specifically for those pollutants can be designed and released into the water to destroy those bacteria and no other organisms.</p>
        <div class="flex-container"><img
        :style="imageStyle" alt="Description" 
        class="water"
          :src="water"
        /></div>
    </section>
</template>

<script>
import water from "@/assets/image/water.jpeg";

export default {
    name: 'AboutSection',  // Update the name here
    components: {
},
    data() {
        return {
            water,
        };
    },
    computed: {
    imageStyle() {
      const width = window.innerWidth;
      if (width < 2000) {
        return { width: '100%' };
      } else if (width < 1024) {
        return { width: '50%' };
      } else {
        return { width: '30%' };
      }
    },
  },
  mounted() {
    window.addEventListener('resize', this.updateImageStyle);
  },
  beforeUnmount() {
    window.removeEventListener('resize', this.updateImageStyle);
  },
  methods: {
    updateImageStyle() {
      this.$forceUpdate(); // Re-evaluate computed properties
    },
  },
};
</script>

<style scoped>

.water{
  width: 700px;
  height: 150px;
  border-radius: 9.694px;
  padding-left: 0px;
  padding-top: 30px;
  margin-bottom: 80px;
  margin-left: 0px;
  margin-right: 0px;
}

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
.flex-container {
  display: flex;
  justify-content: center; /* Center horizontally */
  align-items: center; /* Center vertically */
  
}

.flex-container img {
  max-width: 70%; /* Responsive image */
}
</style>