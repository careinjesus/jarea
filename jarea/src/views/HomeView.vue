<script setup lang="ts">
import MainTemplate from '../template/mainTemplate.vue'

import TheMainWelcome from '../components/TheMainWelcome.vue'
import TheLogin from '../components/TheLogin.vue'
import TheHeader from '../components/TheHeader.vue'
import TheTopnav from '../components/TheTopnav.vue'
import TheFooter from '../components/TheFooter.vue'
import TheCopyright from '../components/TheCopyright.vue'

/********************************************************
import { defineComponent } from 'vue'
export default defineComponent({
  components: {
    MainTemplate,
    TheLogin,
    TheHeader,
    TheTopnav,
    TheMainWelcome,
    TheFooter,
    TheCopyright,
  },
})
*************************************************/
</script>

<template>
  <MainTemplate>
    <template #login><TheLogin /></template>
    <template #header><TheHeader /></template>
    <template #topnav><TheTopnav /></template>
    <template #mainbody><TheMainWelcome /></template>
    <template #footer><TheFooter /></template>
    <template #copyright><TheCopyright /></template>
  </MainTemplate>
</template>

<style lang="scss" scoped></style>

<!-------------------------------------------
-- script --
<script setup lang="ts">
import TheWelcome from '../components/TheMainWelcome.vue'
</script>


-- template --
<template>
  <p>HomeView</p>
  <main>
    <TheWelcome />
  </main>
</template>


----------------------------------------------------->
