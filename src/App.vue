<template>
  <Navigation/>
	<div class="pb-16 max-w-7xl flex-1 mt-8 w-full">
		<router-view></router-view>
	</div>
  <Footer/>
</template>

<script setup lang="ts">
import Navigation from './components/Navigation.vue'
import Footer from './components/Footer.vue'
</script>
