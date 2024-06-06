<script setup>
import { defineProps } from "vue";

const props = defineProps({
  handlesubmit: {
    type: Function,
    required: true,
  },
});
</script>

<template>
  <form @submit="props.handlesubmit">
    <div class="form-group">
      <label for="exampleFormControlInput1">Email address</label>
      <input
        type="email"
        name="email"
        class="form-control"
        id="exampleFormControlInput1"
        placeholder="name@example.com"
      />
    </div>
    <div class="form-group">
      <label for="exampleFormControlInput2">Title</label>
      <input
        type="text"
        name="title"
        class="form-control"
        id="exampleFormControlInput2"
        placeholder="title"
      />
    </div>
    <div class="form-group">
      <label for="exampleFormControlInput3">Auteur</label>
      <input
        type="text"
        name="auteur"
        class="form-control"
        id="exampleFormControlInput3"
        placeholder="auteur"
      />
    </div>
    <div class="form-group">
      <label for="exampleFormControlTextarea1">Contenue</label>
      <textarea
        class="form-control"
        name="contenue"
        id="exampleFormControlTextarea1"
        rows="3"
      ></textarea>
    </div>
    <div id="example">
      <button type="submit" class="btn btn-primary">Submit</button>
    </div>
  </form>
</template>

<style scoped></style>
