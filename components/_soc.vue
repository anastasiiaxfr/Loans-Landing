<template>
  <nav class="soc">
    <NuxtLink v-for="(i, ind) in soc" :key="ind" :to="i.url">
      <NuxtImg :src="i.icon" :alt="i.label" width="24" height="24" />
    </NuxtLink>
  </nav>
</template>

<script setup>
const soc = [
  { icon: "/icon/s1.svg", label: "s1", url: "/" },
  { icon: "/icon/s2.svg", label: "s2", url: "/" },
  { icon: "/icon/s3.svg", label: "s3", url: "/" },
  { icon: "/icon/s4.svg", label: "s4", url: "/" },
];
</script>
