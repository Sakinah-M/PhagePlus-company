<template>
    <section id="advantage" class="mb-5">
        <h2>Added value</h2>
       
        <ul>
            <li> Natural and environmentally friendly method: </li>
            <p>The project does not require harmful chemicals or complex industrial processes in addition to not leaving chemical waste</p>
                <li>  Effective and safe solution:</li>
            <p>Eliminates pathogenic bacteria and pollutants with high efficiency and without affecting the environment or human health and does not change any chemical or physical properties in the water in which it is used. </p>
                <li> Sustainability:  </li>
<p>Phages decompose naturally after completing their mission, which reduces any negative effects and also completely eliminates ultraviolet rays. </p>
                <li> Scalability (applications):</li>
<p>This technology can be used in various types of polluted water, whether in rivers or lakes or even in water treatment plants, fish farming ponds, collection tanks, pumping stations and with bacteria resistant to traditional treatment methods.</p>
       <li> Low cost and economic effectiveness:</li>
       <p> PhagePlus provides a less expensive solution in the long run compared to traditional methods such as chlorine or ozone, making it an economical option that can be easily applied, especially in communities that need low-cost sterilization technologies. </p>
       <li> Use of advanced technology:  </li>
       <p>PhagePlus stands out as one of the projects that combines biotechnology and environmental innovation, contributing to enhancing the role of technology in finding sustainable solutions to environmental challenges.
    </p>
</ul> 
<div class="flex-container"><img
    :style="imageStyle" alt="Description" 
          class="value"
          :src="value"
        /></div>
    </section>
</template>

<script>
import value from "@/assets/image/value.jpeg";

export default {
    name: 'AdvantageSection',  // Update the name here
    components: {
},
    data() {
        return {
            value,
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
.value{
  width:900px;
  height: 200px;
  border-radius: 9.694px;
  padding-left: 0px;
  padding-top: 0px;
  margin-left: 0px;
  margin-right: 0px;
  margin-bottom: 30px;
  margin-top: 10px;

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