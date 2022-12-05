<template>
  <header class="p-8 bg-blue-300 mb-8">
    <div class="flex justify-between">
			<router-link to="Home" class="button">Hjem</router-link>
			<router-link to="Submit" class="button">Indsend Feedback</router-link>
    </div>
  </header>
</template>
<style scoped lang="scss">
.button {
  @apply
  bg-blue-100
  text-black;
}
</style>
