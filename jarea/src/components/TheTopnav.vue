<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { provide } from 'vue'

function updateCURRENTviewOnClick(view: string) {
  console.log(view)
  provide('CURRENTview', 'about')
  console.log(view)
  view = 'kimbap'
  console.log(view)
}

/*****
export default {
  name: ,
  methods: {
    updateCURRENTviewOnClick(view: string) {
      provide('CURRENTview', view)
    }
  },

}
****/
</script>

<template>
  <div class="topnav">
    <RouterLink :to="{ name: 'home' }" class="homeSelect" @click="updateCURRENTviewOnClick('home')"
      >home</RouterLink
    >
    <span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>

    <RouterLink
      :to="{ name: 'value' }"
      class="homeSelect"
      @click="updateCURRENTviewOnClick('value')"
      >value</RouterLink
    >
    <span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>

    <RouterLink
      :to="{ name: 'about' }"
      class="homeSelect"
      @click="updateCURRENTviewOnClick('about')"
      >about</RouterLink
    >
    <span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&#x2022;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>

    <RouterLink
      :to="{ name: 'kimbap' }"
      class="navSelect"
      @click="updateCURRENTviewOnClick('Kimbap')"
      >Kimbap</RouterLink
    >
  </div>
</template>

<style lang="scss" scoped>
.topnav {
  font-size: large;
  text-align: center;
  margin-top: 5px;
  margin-bottom: 5px;
  background-color: white;
}
.homeSelect {
  color: hsl(100, 100%, 10%);
}
.homeSelect:hover {
  background-color: hsl(360, 100%, 96%);
}
.navSelect {
  color: hsl(100, 100%, 10%);
}
.navSelect:hover {
  background-color: hsl(140, 100%, 90%);
}
</style>

<!---------------------------------------------------------------------
-- setup
import { provide, inject } from 'vue'
const welcomeview = inject('CURRENTview')

function updateCurrentView(view: string) {
  alert('updateCurrentView')
  provide('CURRENTview',view) /
  / updateCurrentView.currentView.viewName.value = selectView; return
}

export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++;
    }
  }
}
export default {
  methods: {
    handleClick() {
      this.myFunction();
    },
    myFunction() {
      alert('Button clicked!');
    }
  }
}
export default {
  methods: {
    myMethod(message, number) {
      console.log(message, number);
    }
  }
}

-> below not working

const updateCURRENTviewOnClick = (view: string) => {
  provide('CURRENTview', view)
}

function updateCurrentView(view: string) {
  alert('updateCurrentView')
  provide('CURRENTview', view)
  // updateCurrentView.currentView.viewName.value = selectView; return
}

-- template ---
<RouterLink
  :to="{ name: 'home' }"
  @click="updateCurrentView('home')"
  class="homeSelect"
>home</RouterLink>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<RouterLink
  :to="{ name: 'value' }"
  @click="updateCurrentView('value')"
  class="homeSelect"
>value</RouterLink>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<RouterLink
  :to="{ name: 'about' }"
  @click="updateCurrentView('about')"
  class="homeSelect"
>about</RouterLink>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&#x2022;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<RouterLink
  :to="{ name: 'kimbap' }"
  @click="updateCurrentView('Kimbap')"
  class="navSelect"
>Kimbap</RouterLink>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>

<router-link
  :to="{ name: 'bibimbap' }"
  @click="updateCurrentView('Bibimbap')"
  class="navSelect"
>Bibimbap</router-link>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<router-link :to="{ name: 'dupbap' }" class="navSelect"> Dupbap</router-link>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<router-link :to="{ name: 'sides' }" class="navSelect"> Sides</router-link>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<router-link :to="{ name: 'special' }" class="navSelect"> Special</router-link>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&#x2022;&nbsp;&nbsp;&nbsp;&nbsp;</span>
<router-link :to="{ name: 'drink' }" class="navSelect"> Drink</router-link>

------------------------------------------------------->
