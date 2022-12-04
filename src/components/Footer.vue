<template>
  <footer class="absolute bottom-0 bg-orange-300 px-16 py-4 w-full">
    <div class="footer-wrapper flex justify-between">
      <div class="contact">
        <div class="title">Kontakt</div>
        <div class="flex flex-col text-left">
          <p><span class="font-bold">Email: </span>kk@wexo.dk</p>
          <p><span class="font-bold">Telefon: </span>26166995</p>
          <p><span class="font-bold">Adresse: </span>Sjællandsgade 26</p>
        </div>
      </div>
      <div class="social">
        <div class="title">Socials</div>
        <div class="flex flex-col text-left">
          <div class="someContainer">
            <img src="https://img.icons8.com/color/48/null/facebook-new.png"/>
            <p class="pl-2">Facebook</p>
          </div>
          <div class="someContainer">
            <img src="https://img.icons8.com/color/48/null/instagram-new--v1.png"/>
            <p class="pl-2">Instagram</p>
          </div>
          <div class="someContainer">
            <img src="https://img.icons8.com/color/48/null/twitter--v1.png"/>
            <p class="pl-2">Twitter</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<style scoped>
.title {
  @apply font-bold mb-4 text-lg;
}
.someContainer {
  @apply flex items-center;
}

img {
  height: 25px;
}
</style>