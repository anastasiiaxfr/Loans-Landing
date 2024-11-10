<template>
  <section class="section section_about" id="about">
    <div class="container">
      <div class="row_1">
        <div>
          <h2>
            About us
          </h2>
          <img :src="img" alt="About Us" />

          <p>
            QuickFunds- Your trusted financial partner for loans. Quick approvals, competitive rates, and personalized
            solutions to meet your unique needs. Empowering you to achieve your financial goals. Apply online today!
          </p>
        </div>
        <div>
          <Form />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import img from "~/assets/img/img6.svg";
import Form from "~/components/_form.vue";
</script>
