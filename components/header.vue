<template>
  <header class="header">
    <div class="container">
      <NuxtLink to="/" class="logo">
        <img :src="logoImg" alt="Logo" />
      </NuxtLink>
      <nav class="header-menu">
        <a v-for="(item, index) in menu" :key="index" :href="item.url">
          {{ item.label }}
        </a>
      </nav>
      <div class="header-btns">
        <a class="btn" href="#about">Contact us</a>
        <button type="button" class="header-toggler" @click="toggleDrawer">
          <NuxtImg src="/icon/menu.svg" alt="menu" width="24" height="24" />
        </button>
      </div>
    </div>
  </header>
  <aside class="drawer" :class="{ show: isDrawerOpen }">
    <div class="drawer-header">
      <NuxtLink to="/" class="logo">
        <img :src="logoImg" alt="Logo" />
      </NuxtLink>
      <button type="button" class="header-toggler" @click="toggleDrawer">
        <NuxtImg src="/icon/close.svg" alt="close" width="24" height="24" />
      </button>
    </div>
    <nav class="drawer-menu">
      <NuxtLink v-for="(item, index) in menu" :key="index" :to="item.url" @click="toggleDrawer">
        {{ item.label }}
      </NuxtLink>
    </nav>
    <NuxtLink class="btn" to="#contacts" @click="toggleDrawer">Contact us</NuxtLink>
  </aside>
</template>

<script setup>
import logoImg from "~/assets/img/logo.svg";

const isDrawerOpen = ref(false);

const toggleDrawer = () => {
  isDrawerOpen.value = !isDrawerOpen.value;
};

const menu = [
  { url: "/", label: "Home" },
  { url: "#services", label: "Services" },
  { url: "#str", label: "How we work?" },
  { url: "#about", label: "About Us" },
];
</script>
