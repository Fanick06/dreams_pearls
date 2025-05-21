<script setup>
function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' });
}
</script>

<template>

  <footer class="bg-[#1f1f1f] text-white py-10 px-6 mt-2">
    <div class="max-w-6xl mx-auto grid md:grid-cols-4 sm:grid-cols-2 gap-8 text-sm">

      <!-- Logo / Présentation -->
      <div>
        <!-- <img src="../assets/LOGO.png" alt=""> -->
        <h2 class="text-xl font-bold text-[#d8b38f]">Dreams_Pearls</h2>
        <p class="mt-2 text-white-300 text-base">
          Des cafés d’exception et des snacks faits maison, avec amour.
        </p>
      </div>

      <!-- Horaires -->
      <div>
        <h3 class="text-xl font-semibold mb-2 text-[#d8b38f]">Horaires</h3>
        <ul class="text-white-300 text-base">
          <li>Lundi - Vendredi : 7h - 20h</li>
          <li>Samedi : 8h - 18h</li>
          <li>Dimanche : Fermé</li>
        </ul>
      </div>

      <!-- Contact -->
      <div>
        <h3 class="text-xl font-semibold mb-2 text-[#d8b38f]">Contact</h3>
        <ul class="text-white-300 text-base space-y-2">
          <li class="flex items-center gap-2"><img src="../assets/localisation.png" alt="local" class="w-5 h-5">
            Cotonou, Bénin</li>
          <li class="flex items-center gap-2"><img src="../assets/tel.png" alt="tel" class="w-5 h-5"> +229 01 65 59 16
            12</li>
          <li class="flex items-center gap-2"><img src="../assets/msg.png" alt="msg" class="w-5 h-5">
            fanickcoffee@gmail.com</li>
        </ul>
      </div>

      <!-- Réseaux sociaux -->
      <div>
        <h3 class="text-xl font-semibold mb-2 text-[#d8b38f]">Suivez-nous</h3>
        <div class="flex gap-8 mt-2 text-base">
          <a href="https://facebook.com" target="_blank">
            <img src="../assets/icons8-facebook-nouveau-50.png" alt="fb" class="w-8 h-8">
          </a>
          <a href="https://instagram.com" target="_blank">
            <img src="../assets/instagr.png" alt="inst" class="w-8 h-8">
          </a>
          <a href="https://wa.me/2250707070707" target="_blank">
            <img src="../assets/whatsapp.png" alt="whatsapps" class="w-8 h-8">
          </a>
        </div>

        <!-- Newsletter -->
        <form @submit.prevent class="mt-6">
          <input type="email" placeholder="Votre email"
            class="w-full p-2 rounded bg-gray-800 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-[#ee7721]" />
          <button
            class="mt-2 w-full bg-[#d8b38f] text-white py-2 rounded transition">S'inscrire</button>
        </form>

      </div>
    </div>



    <div class="text-center text-white-400 mt-10 text-lg border-t border-gray-700 pt-4">
      &copy; {{ new Date().getFullYear() }} Dreams_Pearls. Tous droits réservés.
    </div>

    <button @click="scrollToTop"
      class="fixed bottom-6 right-6 bg-[#d8b38f] text-white p-3 rounded-lg shadow-lg transition z-50">
      ↑
    </button>
  </footer>

</template>

<style scoped></style>
