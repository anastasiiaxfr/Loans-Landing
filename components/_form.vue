<template>
  <form class="form" action="/" method="POST" noValidate @submit.prevent="formSend">
    <div class="form-row">
      <label for="name">Your Name</label>
      <input v-model="name" type="text" required name="name" id="name" />
    </div>
    <div class="form-row">
      <label for="tel">Phone number</label>
      <input v-model="tel" type="text" required name="tel" id="tel" />
    </div>
    <div class="form-row">
      <label for="email">Email address</label>
      <input v-model="email" type="email" required name="email" id="email" />
    </div>
    <div class="form-row">
      <button type="submit" class="btn" :disabled="!isFormValid">Send</button>
    </div>
  </form>
</template>

<script setup>
import { ref, computed } from "vue";

const name = ref("");
const tel = ref("");
const email = ref("");

const isFormValid = computed(() => {
  return name.value.trim() !== "" && tel.value.trim() !== "" && email.value.trim() !== "";
});

const formSend = () => {
  alert("Form Send");
  // Reset form fields
  name.value = "";
  tel.value = "";
  email.value = "";
};
</script>
