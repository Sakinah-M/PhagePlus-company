<template>
    <section id="services" class="mb-5">
        <h2>Our Services</h2>
        <ol> 
            <li> Research and Development:</li>
            <P>Genetically modifying bacteriophages to be able to specifically target harmful bacteria. </P>
            <li>  Laboratory experiments: </li>
            <p>Identifying the type of pollutants by analyzing a water sample and designing phages, then testing the effectiveness of the modified phages in simulated aquatic environments to ensure their ability to eliminate bacteria without affecting the environment. </p>
            <li> Application in field sites: </li>
            <p>Applying the modified phages in field sites such as water treatment plants or in polluted water sources. </p>
            <li> Monitoring and evaluation:</li>
            <p>Monitoring the results of the treatment in terms of the effectiveness of the phages in eliminating bacteria, and after the disinfection process is completed, exposing the water to ultraviolet rays to ensure that they do not affect the environment.</p>
            <div class="flex-container"><img
        :style="imageStyle" alt="Description" 
          class="micros"
          :src="micros"
        /></div>
        </ol>
    </section>
</template>

<script>
import micros from "@/assets/image/micros.jpeg";

export default {
    name: 'ServicesSection',  // Update the name here
    components: {
},
    data() {
        return {
            micros,
        };
    },
    computed: {
    imageStyle() {
      const width = window.innerWidth;
      if (width < 2000 ) {
        return { width: '100%'};
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
.micros{
  width: 900px;
  height: 200px;
  border-radius: 9.694px;
  padding-left: 0px;
  padding-top: 0px;
  margin-left: 0px;
  margin-right: 0px;
  margin-bottom: 70px;
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