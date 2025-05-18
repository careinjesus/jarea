<script setup lang="ts">
import MainTemplate from '../template/mainTemplate.vue'

import TheMainWelcome from '../components/TheMainWelcome.vue'
import TheLogin from '../components/TheLogin.vue'
import TheHeaderWelcome from '../components/TheHeaderWelcome.vue'
import TheTopnav from '../components/TheTopnav.vue'
import TheFooter from '../components/TheFooter.vue'
import TheCopyright from '../components/TheCopyright.vue'
</script>

<template>
  <MainTemplate>
    <template #login><TheLogin /></template>
    <template #header><TheHeaderWelcome /></template>
    <template #topnav><TheTopnav /></template>
    <template #mainbody><TheMainWelcome /></template>
    <template #footer><TheFooter /></template>
    <template #copyright><TheCopyright /></template>
  </MainTemplate>
</template>

<style lang="scss" scoped></style>

<!--------------------------------------------
-- script --
import { defineComponent } from 'vue'
export default defineComponent({
  components: {
    MainTemplate,
    TheLogin,
    TheHeaderWelcome,
    TheTopnav,
    TheMainWelcome,
    TheFooter,
    TheCopyright,
  },
})

- style -
@media (min-width: 1024px)
{ .about { min-height: 100vh; display: flex; align-items: center; } }

------------------------------------------------->
