<template>
  <footer class="footer">
    <div class="footer-top">
      <div class="container">
        <div class="footer-info">
          <NuxtLink to="/" class="logo">
            <img :src="logoImg" alt="Logo" />
          </NuxtLink>
          <div class="footer-note">
            Our mission is to empower individuals and businesses by providing them with the financial resources they
            need to achieve their goals.
          </div>
          <Soc />
        </div>
        <div>
          <div class="footer-nav">
            <div>
              <div class="footer-nav-title">OUR SERVICES</div>
              <hr class="divider" />
              <ul>
                <li v-for="(i, ind) in nav" :key="ind">
                  <a :href="i.url">{{ i.label }}</a>
                </li>
              </ul>
            </div>
            <div>
              <div class="footer-nav-title">CONTACT US</div>
              <hr class="divider" />
              <nav class="contacts">
                <p v-for="(i, ind) in contacts" :key="ind">
                  <a href="i.url">
                    <img :src="i.icon" :alt="i.label" width="24" height="24" /><span v-html="i.label"></span>
                  </a>
                </p>
              </nav>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-btm">
      <div class="container">
        <nav>
          <NuxtLink to="/terms">Terms and Conditions </NuxtLink>
          <NuxtLink to="/policy">Privacy Policy </NuxtLink>
          <NuxtLink to="/cookie">Cookie Policy </NuxtLink>
        </nav>
      </div>
    </div>
  </footer>
</template>

<script setup>
import logoImg from "~/assets/img/logo-w.svg";
import i1 from "~/assets/img/icon/s5.svg";
import i2 from "~/assets/img/icon/s6.svg";
import i3 from "~/assets/img/icon/s7.svg";
import Soc from "~/components/_soc.vue";

const nav = [
  { url: "/", label: "Personal loan" },
  { url: "/", label: "Business loan" },
  { url: "/", label: "Education loan" },
  { url: "/", label: "Auto loan" },
];

const contacts = [
  {
    icon: i1,
    url: "tel:+919999999999",
    label: "+91 99999 99999",
  },
  {
    icon: i2,
    url: "mailto:xyzfh5@gmail.com",
    label: "xyzfh5@gmail.com",
  },
  {
    icon: i3,
    url: "/",
    label: "Address line-1 <br>Address line-2, <br>city, state-pin code.",
  },
];
</script>
