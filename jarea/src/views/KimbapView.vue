<script setup lang="ts">
import MainTemplate from '../template/mainTemplate.vue'
import TheLogin from '../components/TheLogin.vue'
import TheHeader from '../components/TheHeader.vue'
import TheTopnav from '../components/TheTopnav.vue'
import TheKimbap from '../components/TheMainKimbap.vue'
import TheFooter from '../components/TheFooter.vue'
import TheCopyright from '../components/TheCopyright.vue'
</script>

<template>
  <MainTemplate>
    <template #login><TheLogin /></template>
    <template #header><TheHeader /></template>
    <template #topnav><TheTopnav /></template>
    <template #mainbody><TheKimbap /></template>
    <template #footer><TheFooter /></template>
    <template #copyright><TheCopyright /></template>
  </MainTemplate>
</template>

<style lang="scss" scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<!-----------------------------------
-- script --
import MainTemplate from '@/template/mainTemplate.vue'
import { defineComponent } from 'vue'
export default defineComponent({
  components: {
    MainTemplate,
    TheLogin,
    TheHeader,
    TheTopnav,
    TheKimbap,
    TheFooter,
    TheCopyright,
  },
})

-- style --

---------------------------------------------->>
