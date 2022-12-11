<template>
  <nav class="p-4 w-full bg-gray-800">
		<ul class="flex justify-between">
			<router-link tag="li" to="Home" class="button">Hjem</router-link>
			<router-link tag="li" to="Submit" class="button">Indsend Feedback</router-link>
		</ul>
  </nav>
</template>
<style scoped lang="scss">
.button {
  @apply
  bg-blue-100
  text-black;
}
</style>
