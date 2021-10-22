<template>
  <div class="home">
    <div v-for="item in 10" :key="item">
      <app-card
        imgUser="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80"
        imgCard="https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80"
        username="Samanta Blure"
        :price="400"
      ></app-card>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import AppCard from "@/components/AppCard.vue";

export default {
  name: "Home",
  components: {
    AppCard,
  },
};
</script>
