<template>
    <section id="contact">
        <h2>Contact Us</h2>
        <p>Contact us to book a service or if you have any questions about the services provided.
        </p>
        <form @submit.prevent="submitForm">
            <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" class="form-control" id="name" v-model="name" required>
            </div>
            <div class="mb-3">
                <label for="email" class="form-label">Email</label>
                <input type="email" class="form-control" id="email" v-model="email" required>
            </div>
            <div class="mb-3">
                <label for="message" class="form-label">Message</label>
                <textarea class="form-control" id="message" v-model="message" required></textarea>
            </div>
            <button type="submit" class="btn btn-orange">Send</button>
        </form>
    </section>
</template>

<script>
export default {
    name: 'ContactSection',  // Update the name here

    data() {
        return {
            name: '',
            email: '',
            message: ''
        };
    },
    methods: {
        submitForm() {
            alert(`Name: ${this.name}\nEmail: ${this.email}\nMessage: ${this.message}`);
            // Reset the form
            this.name = '';
            this.email = '';
            this.message = '';
        }
    }
}
</script>
<style scoped>
.btn{
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
</style>