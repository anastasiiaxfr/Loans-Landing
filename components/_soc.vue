<template>
  <nav class="soc">
    <NuxtLink v-for="(i, ind) in soc" :key="ind" :to="i.url">
      <img :src="i.icon" :alt="i.label" width="24" height="24" />
    </NuxtLink>
  </nav>
</template>

<script setup>
import i1 from "~/assets/img/icon/s1.svg";
import i2 from "~/assets/img/icon/s2.svg";
import i3 from "~/assets/img/icon/s3.svg";
import i4 from "~/assets/img/icon/s4.svg";

const soc = [
  { icon: i1, label: "s1", url: "/" },
  { icon: i2, label: "s2", url: "/" },
  { icon: i3, label: "s3", url: "/" },
  { icon: i4, label: "s4", url: "/" },
];
</script>
