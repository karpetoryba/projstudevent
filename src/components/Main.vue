<script setup>
import { ref } from "vue";
import FormComponent from "./FormComponent.vue";

const handleSubmit = (e) => {
  e.preventDefault();
  const formData = new FormData(e.target);
  const data = Object.fromEntries(formData.entries());
  console.log("Form Data:", data);
};

const example = ref({
  name: "Vue.js",
  greet(event) {
    alert("slick");

    if (event) {
      alert("pas de click");
    }
  },
});
</script>

<template>
  <p>EVENTS LIST</p>
  <FormComponent :handlesubmit="handleSubmit"></FormComponent>
</template>

<style scoped></style>
