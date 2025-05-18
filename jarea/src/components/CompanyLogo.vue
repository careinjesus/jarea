<script setup lang="ts">
import { RouterLink } from 'vue-router'
import urlCompanyLogo from '../assets/images/companyLogo.png'
</script>

<template>
  <div class="companyLogo">
    <router-link :to="{ name: 'home' }">
      <img :src="urlCompanyLogo" alt="Company Logo Url" />
    </router-link>
  </div>
</template>

<style lang="scss" scoped>
.companyLogo {
  /* display: flex;  commented because pointer effective for the grid bloack, not the image itself */
  align-items: center;

  img {
    width: 45%;
  }
}
</style>
