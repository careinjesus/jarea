<script setup lang="ts">
import { inject } from 'vue'

import companyLogo from './CompanyLogo.vue'
import companyLogoText from './headerCompanyName.vue'

const currentView = inject('CURRENTview')
</script>

<template>
  <div class="headerBody">
    H--{{ currentView }}--D

    <div class="logo"><companyLogo /></div>
    <div><companyLogoText /></div>

    <div></div>
    <div class="mainDish">{{ currentView }}</div>
    <div></div>
    <div></div>

    <!--
  <div class="dishes"> <themeDishes /> </div>
  <div class="empty"></div>                                 -- blank column --

  --></div>
</template>

<style lang="scss" scoped>
.headerBody {
  width: 100%;
  height: 120px;

  display: grid;
  grid-template-columns: repeat(7, 1fr); /* column-count: 3 */
  align-items: center;

  background-color: hsl(360, 100%, 96%);

  .logo {
    text-align: right;
  }
  .logoTxt {
    text-align: left;
  }
  .points {
    text-align: right;
  }
  .mainDish {
    text-align: center;
    font-size: xx-large;
  }
  .dishes {
    text-align: left;
  }
  .empty {
    height: 100%;
  }
}
</style>

<!------------------------------------------------------------
** Options API => converted to Composition API using <script setup

import { defineComponent } from 'vue'
export default defineComponent({
  components: {
    companyLogo,
    companyLogoText,
  },
  data() {
    return {
      currentView: inject('CURRENTview'),
    }
  },
})



let viewTitle = this.$app.config.globalProperties.globalCurrentView;
let viewDesc =''; switch (viewTitle) { case 'home': { viewDesc = 'home'; }; break; case 'value':
viewTitle = 'value'; break; case 'about': viewTitle = 'about'; break; case 'Kimbap': viewTitle =
'Kimbap'; break; case 'Bibimbap': viewTitle = 'Bibimbap'; break; case 'Dupbap': viewTitle =
'Dupbap'; break; case 'Sides': viewTitle = 'Sides'; break; case 'Special': viewTitle = 'Special';
break; case 'Drink': viewTitle = 'Drink'; break; default: viewTitle = 'home'; } ******* end


------------------------------------------>>
