<template>
    <header>
        <nav class="navbar navbar-expand-lg navbar-light">
            <div class="container">
                <img
          class="logo"
          :src="logo"
        />
                <a class="navbar-brand" href="#">PHAGEPLUS
                    <p>Innovation Water Sterilization Technology</p>
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav ms-auto">
                        <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
                        <li class="nav-item"><a class="nav-link" href="#services">Services</a></li>
                        <li class="nav-item"><a class="nav-link" href="#advantage">Aded Value</a></li>
                        <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
import logo from "@/assets/image/logo.jpeg";

export default {
    name: 'NavbarSection',  // Update the name here

    components: {
},
    data() {
        return {
            logo,
        }
    }
};
</script>
<style scoped>
.logo {
  background-image: url("@/assets/image/logo.jpeg");
  background-repeat: no-repeat;
  background-position: 0px left;
  width: 120px;
  height: 120px;
  border-radius: 9.694px;
  padding-left: 0px;
  padding-top: 0px;
  margin-left: 0px;
  margin-right: 20px;
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

</style>