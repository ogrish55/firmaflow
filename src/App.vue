<template>
  <div>
    <Header/>
    <router-view class="pb-16"></router-view>
    <Footer/>
  </div>
</template>

<script setup lang="ts">
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
</script>
