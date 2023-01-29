<template>
  <div
    class="flex flex-col min-h-screen font-Roboto bg-weather-primary"
  >
      <div>
    <SiteNavigation />
    <RouterView class="flex-1" v-slot="{ Component }">
      <Transition name="page">
        <component :is="Component" />
      </Transition>
    </RouterView>
  </div>

    <div class="pt-8 mt-1">
       <div> <h4 class="text-center  text-white text-2xl">What are the Cause for Global Warming ?</h4></div>
        <div class="grid gap-4 grid-cols-2 grid-rows-2">      
       <img src="./assets/humid_person.jpg" class="max-w-full h-auto w-full p-5  " alt="..." />
       <img src="./assets/humid_location.jpg" class="max-w-full h-auto w-full p-5  " alt="..." />
      </div> 
   </div>
   

  </div>
</template>

<script setup>
import { RouterView } from "vue-router";
import SiteNavigation from "./components/SiteNavigation.vue";
</script>

<style>
.page-enter-active {
  transition: 600ms ease all;
}

.page-enter-from {
  opacity: 0;
}
</style>
