<template>
  <Header/>
  <div class="mx-auto" style="max-width: 1280px;">
    <router-view class="pb-16"></router-view>
  </div>
  <Footer/>
</template>

<script setup lang="ts">
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
</script>
