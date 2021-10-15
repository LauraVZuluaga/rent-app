<template>
  <div class="home">
    <app-card></app-card>
  </div>
</template>

<script>
// @ is an alias to /src
import AppCard from '@/components/AppCard.vue'

export default {
  name: 'Home',
  components: {
    AppCard
  }
}
</script>
