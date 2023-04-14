<template>
  <div class="contact-main">
  <div class="contact-container">
    <div class="contact-info">
      <h2 class="contact-info-heading">Contact Information</h2>

      <div class="contact-item">
        <i class="fas fa-envelope icon"></i>
        <p>contact@company.com</p>
      </div>
      <div class="contact-item">
        <i class="fas fa-phone icon"></i>
        <p>+1-123-456-7890</p>
      </div>
      <div class="contact-item">
        <i class="fa fa-map-marker icon" aria-hidden="true"></i>
        <p>+1-123-456-7890</p>
      </div>
      <h2 class="contact-info-heading">Social Media Channel</h2>
      <div class="contact-item">
        <i class="fa-brands fa-facebook-f social-icon" ></i>
        <i class="fab fa-twitter social-icon"></i>
        <i class="fa-brands fa-github social-icon"></i>
        <i class="fa-brands fa-linkedin-in social-icon"></i>
      </div>
    </div>
    <div class="contact-form">
      <h2 class="form-heading">Fill up the form and our team will get back to <br> you within 24 hours</h2>
      <form @submit.prevent="submitForm" class="main-form">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="phone">Phone</label>
          <input
            type="tel"
            id="phone"
            v-model="phone"
            ref="phone"
            :class="{ 'is-invalid': !isValidPhone }"
            @blur="validatePhone"
            required
            pattern="^\d{10}$"
          />
          <div v-if="!isValidPhone" class="invalid-feedback">
            Phone number must be 10 digits long
          </div>
        </div>
        <div class="form-group">
          <label for="subject">Subject</label>
          <input type="text" id="subject" v-model="subject" required>
        </div>
        <div class="form-group message">
          <label for="message">Message</label>
          <textarea id="message" v-model="message" rows="5" required></textarea>
        </div>
        <div class="btn">
          <button class="btn-submit" type="submit">Submit</button>
        </div>
        
      </form>
    </div>
  </div>
</div>
</template>

<script>
import "@/styles/contact.css";
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      name: "",
      email: "",
      phone: "",
      subject: "",
      message: "",
      isValidPhone: true,
    };
  },
  methods: {
    validatePhone() {
      const regex = /^\d{10}$/;
      this.isValidPhone = regex.test(this.phone);
    },
    submitForm(e) {
      if (this.$refs.phone.checkValidity()) {
       alert("Form submitted")
        console.log("Form submitted");
      } else {
        // display error message or highlight invalid fields
        console.log("Form is invalid");
      }
    },
  },
});
</script>
