<script setup lang="ts">
import headerCompanyLogo from '../components/headerCompanyLogo.vue'
import headerCompanyName from '../components/headerCompanyName.vue'
import headerMessage from '../components/headerMessage.vue'
</script>

<template>
  <div class="headerStyle">
    <div class="logo"><headerCompanyLogo /></div>
    <div class="companyname"><headerCompanyName /></div>
    <div class="message"><headerMessage /></div>
    <div class="empty"></div>
    <div class="empty"></div>
    <div class="empty"></div>
    <!-- blank column -->
  </div>
</template>

<style lang="scss" scoped>
.headerStyle {
  width: 100%;
  height: 165px;

  display: grid;
  grid-template-columns: repeat(7, 1fr); /* column-count: 3 */
  align-items: center;

  background-color: hsl(360, 100%, 96%);

  .logo {
    text-align: right;
  }
  .companyanme {
    text-align: left;
  }
  .message {
    text-align: center;
  }
  .empty {
    height: 100%;
  }
}
</style>
