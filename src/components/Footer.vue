<template>
  <footer class="bottom-0 px-16 py-4 w-full mt-auto">
    <div class="footer-wrapper flex justify-between">
      <div style="min-width: 210px;" class="contact">
        <div class="title">Kontakt</div>
        <div class="flex flex-col text-left">
          <a class="text-inherit hover:text-white hover:underline" href="mailto:kk@wexo.dk" target="_blank"><span class="font-bold">Email: </span>kk@wexo.dk</a>
          <a class="text-inherit hover:text-white hover:underline" href="tel:+4526166995" target="_blank"><span class="font-bold">Telefon: </span>26166995</a>
          <p><span class="font-bold">Adresse: </span>Sjællandsgade 26</p>
        </div>
      </div>
      <div style="min-width: 210px;" class="social">
        <div class="title">Socials</div>
        <div class="flex flex-col text-left items-end">
          <div class="someContainer">
            <img src="https://img.icons8.com/color/48/null/facebook-new.png"/>
            <p class="pl-4">Facebook</p>
          </div>
          <div class="someContainer">
            <img src="https://img.icons8.com/color/48/null/instagram-new--v1.png"/>
            <p class="pl-4">Instagram</p>
          </div>
          <div class="someContainer">
            <img src="https://img.icons8.com/color/48/null/twitter--v1.png"/>
            <p class="pl-4">Twitter</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<style scoped>
.title {
  @apply font-bold mb-4 text-lg border-b border-sky-100;
}
.someContainer {
  @apply flex items-center w-fit justify-between;
 min-width: 125px;
}

img {
  height: 25px;
}
</style>