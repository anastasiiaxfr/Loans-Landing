<template>
  <section class="section section_services">
    <div class="container text-center">
      <h2 class="">Our Services</h2>
      <div class="cards">
        <article class="card" v-for="(card, ind) in services" :key="ind">
          <NuxtImg :src="card.icon" width="64" height="64" />
          <div class="card-title">{{ card.title }}</div>
          <div class="card-desc">{{ card.desc }}</div>
          <NuxtLink class="btn-bd">{{ card.btn.label }}</NuxtLink>
        </article>
      </div>
      <NuxtLink class="btn" to="#">View more</NuxtLink>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    icon: "i1.svg",
    title: "Personal loan",
    desc: "Personal loans provide borrowers with flexibility in how they use the funds.",
    btn: {
      label: "Apply now",
      url: "#",
    },
  },
  {
    icon: "i2.svg",
    title: "Business loan",
    desc: "Business Loan Services provide financial assistance to businesses for various purposes..",
    btn: {
      label: "Apply now",
      url: "#",
    },
  },
  {
    icon: "i3.svg",
    title: "Auto loan",
    desc: "Auto Loan Services provide financing options for individuals businesses to purchase a vehicle.",
    btn: {
      label: "Apply now",
      url: "#",
    },
  },
];
</script>
