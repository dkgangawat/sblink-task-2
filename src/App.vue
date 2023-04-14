<template>
  <div>
    <Navbar />
    <section class="sec-1">
      <div class="container">
      <div class="text-container">
        <h3>AnyTime, anywhere Learn on your schedule from any device</h3>
        <p>We Believe everyone has the capcity to be creative <br> Course Pro is a place where people develop their own
          potential</p>
        <button>Let's Get Started</button>
      </div>
      <div class="img-container">
        <img src="@/assets/images/intro.png" alt="intro image" />
      </div>
    </div>
    </section>
    <section class="statistics">
      <div class="statistics__item">
        <h2 class="statistics__title">Total Students</h2>
        <p class="statistics__value">{{ totalStudents }}</p>
      </div>
      <div class="statistics__item">
        <h2 class="statistics__title">Partners</h2>
        <p class="statistics__value">{{ partners }}</p>
      </div>
      <div class="statistics__item">
        <h2 class="statistics__title">Affiliate Distribution</h2>
        <p class="statistics__value">{{ affiliateDistribution }}</p>
      </div>
    </section>
    <section class="courses">
      <div class="headings">
      <h3 class="section-heading">Courses</h3>
      <h2 class="section-sub-heading">Our most popular courses</h2>
    </div>
      <div class="courses-container">
        <template v-for="(course, x) in courses" :key="x">
          <Card :course="course" />
        </template>
      </div>
    </section>
    <section class="earner">
      <div class="headings">
      <h3 class="section-heading" style="text-align: left;">Top Earner</h3>
      <h2 class="section-sub-heading" style="text-align: left;">Transformng your ideas <br>into reality</h2>
    </div>
      <div class="earners-container">
        <template v-for="(data, index) in Earners" :key="index">
          <EarnerCard :cardData="data" />
        </template>
      </div>
    </section>
    <section class="Refer">
      <div class="headings">
      <h3 class="section-heading" style="text-align: left;">Refer</h3>
      <h2 class="section-sub-heading" style="text-align: left;">How it's work</h2>
      </div>
      <div>
        <img src="@/assets/images/Refer.png" alt="Refer" />
      </div>
    </section>
    <section class="testinomial">
      <div class="headings">
      <h3 class="section-heading" style="text-align: left;">Testimonials</h3>
      <h2 class="section-sub-heading" style="text-align: left;">Check out What Our <br> Students Think About Us</h2>
    </div>
      <div class="testinomial-cards">
        <template v-for="(data, index) in Testinomial" :key="index">
          <TestinomialCard :testimonial="data" />
        </template>
      </div>

    </section>
    <section class="contact">
      <h3 class="section-heading" >Contact Us</h3>
      <h2 class="section-sub-heading">Reach Out with any <br> question you have</h2>
      <div class="main-conatact">
        <ContactUs />
      </div>
    </section>
    <Footer/>
  </div>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.min.css'

import Navbar from '@/components/Navbar.vue';
import courses from "@/courses.js"
import Card from '@/components/Card.vue';
import EarnerCard from '@/components/EarnerCard.vue';
import Earners from "@/Earners.js"
import Refer from "@/assets/images/Refer.vue"
import TestinomialCard from './components/TestinomialCard.vue';
import Testinomial from "@/Testinomial.js"
import ContactUs from "@/components/Contact.vue"
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    Navbar,
    Card,
    EarnerCard,
    Refer,
    Footer,
    TestinomialCard,
    ContactUs,
  },
  data() {
    return {
      courses,
      Earners,
      Testinomial,
      totalStudents: 5140,
      partners: 4123,
      affiliateDistribution: '4.18 lac'
    }
  },
};
</script>
import '@/styles/app.css'
<style>
/* Add styles for App component here */
</style>
