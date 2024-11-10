import { NuxtLink } from '../../.nuxt/components';
<template>
  <section class="section section_hero">
    <div class="container">
      <div class="row_1">
        <div>
          <hgroup>
            <h1>
              Quick and Easy Loans for Your Financial Needs.
            </h1>
            <p>
              Our loan services offer a hassle-free and streamlined borrowing experience, providing you with the funds
              you need in a timely manner to meet your financial requirements.
            </p>
          </hgroup>
          <NuxtLink class="btn-bd">
            Get started
          </NuxtLink>
        </div>
        <div>
          <img :src="img" alt="Logo" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import img from "~/assets/img/img1.svg";
</script>
