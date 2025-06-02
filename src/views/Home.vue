<script setup>

</script>

<template>
  <section class="text-center w-full h-170 bg-cover py-70 bg-[url(../assets/caf.jpg)] bg-no-repeat text-white">
    <div class=" ">
      <h1 class="text-6xl text-center font-bold mb-4 ">Dreams_Pearls</h1>
      <p class="text-2xl ">Découvrez notre collection élégante de perles.</p>

      <router-link to="/produit"
        class="inline-block bg-[#fc6b07] hover:bg-[#fc6907e2] text-white font-semibold py-3 px-6 rounded-full shadow-lg transition-all duration-300 mt-6 ">
        Nos Produit
      </router-link>

    </div>
  </section>


  <section class="bg-white py-16 px-6 md:px-20 mt-20">
    <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center md:items-start gap-10">

      <!-- Texte à gauche -->
      <div class="md:w-1/2">
        <h2 class="text-3xl md:text-4xl font-extrabold text-[#fc6b07] leading-tight mb-4">
          Explorez l’univers unique <br />
          <span class="text-black">des perles Dreams_Pearls</span>
        </h2>
        <p class="text-gray-700 mb-6">
          Découvrez nos perles artisanales soigneusement sélectionnées pour leur éclat, leur couleur vibrante
          et leur qualité supérieure. Parfaites pour vos créations ou pour offrir.
        </p>
        <router-link to="/contact">
          <button
            class="mt-2 px-5 py-2 border border-black rounded-full hover:bg-black hover:text-white transition font-medium">
            Nous contacter →
          </button>
        </router-link>
      </div>

      <!-- Cartes en escalier à droite -->
      <div class="md:w-1/2 flex space-x-6">
        <!-- Carte 1 -->
        <router-link to="/produit" class="transform hover:scale-105 transition duration-300">
          <div class="bg-white rounded-xl overflow-hidden shadow-lg -mt-4 w-[250px]">
            <img src="../assets/tui.webp" alt="Perles Dorées"
              class="w-full h-60 object-cover" />
            <div class="bg-[#fc6b07] text-white text-center py-2 font-semibold text-sm">Perles Dorées</div>
          </div>
        </router-link>

        <!-- Carte 2 (un peu plus haute) -->
        <router-link to="/produit" class="transform hover:scale-105 transition duration-300">
          <div class="bg-white rounded-xl overflow-hidden shadow-lg -mt-15 w-[250px]">
            <img src="../assets/pi.jpg" alt="Perles Colorées"
              class="w-full h-60 object-cover" />
            <div class="bg-[#fc6b07] text-white text-center py-2 font-semibold text-sm">Perles Colorées
            </div>
          </div>
        </router-link>

        <!-- Carte 3 (encore plus haute) -->
        <router-link to="/produit" class="transform hover:scale-105 transition duration-300">
          <div class="bg-white rounded-xl overflow-hidden shadow-lg -mt-27 w-[250px]">
            <img src="../assets/mp.jpg" alt="Perles de Luxe"
              class="w-full h-60 object-cover" />
            <div class="bg-[#fc6b07] text-white text-center py-2 font-semibold text-sm">Perles de Luxe</div>
          </div>
        </router-link>
      </div>
    </div>
  </section>

  <!--Produits-->

  <section class="bg-gray-50 py-16 px-6 md:px-20">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center text-[#fc6b07] mb-12">
        Nos Best-sellers
      </h2>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- Produit 1 -->
        <router-link to="/produit"
          class="block bg-white rounded-xl shadow hover:shadow-lg hover:scale-105 transition duration-300 overflow-hidden">
          <img src="https://via.placeholder.com/300x200?text=Perle+Or" alt="Perle Or"
            class="w-full h-48 object-cover" />
          <div class="p-4 text-center">
            <h3 class="font-semibold text-lg text-gray-800">Perle Or</h3>
            <p class="text-[#fc6b07] font-bold my-2">9,90€</p>
            <button class="bg-[#fc6b07] text-white px-4 py-1 rounded-full text-sm hover:bg-amber-700 transition">
              Voir le produit
            </button>
          </div>
        </router-link>

        <!-- Produit 2 -->
        <router-link to="/produit"
          class="block bg-white rounded-xl shadow hover:shadow-lg hover:scale-105 transition duration-300 overflow-hidden">
          <img src="https://via.placeholder.com/300x200?text=Perle+Cristal" alt="Perle Cristal"
            class="w-full h-48 object-cover" />
          <div class="p-4 text-center">
            <h3 class="font-semibold text-lg text-gray-800">Perle Cristal</h3>
            <p class="text-[#fc6b07] font-bold my-2">12,50€</p>
            <button class="bg-[#fc6b07] text-white px-4 py-1 rounded-full text-sm hover:bg-amber-700 transition">
              Voir le produit
            </button>
          </div>
        </router-link>

        <!-- Produit 3 -->
        <router-link to="/produit"
          class="block bg-white rounded-xl shadow hover:shadow-lg hover:scale-105 transition duration-300 overflow-hidden">
          <img src="https://via.placeholder.com/300x200?text=Perle+Noire" alt="Perle Noire"
            class="w-full h-48 object-cover" />
          <div class="p-4 text-center">
            <h3 class="font-semibold text-lg text-gray-800">Perle Noire</h3>
            <p class="text-[#fc6b07] font-bold my-2">7,20€</p>
            <button class="bg-[#fc6b07] text-white px-4 py-1 rounded-full text-sm hover:bg-amber-700 transition">
              Voir le produit
            </button>
          </div>
        </router-link>

        <!-- Produit 4 -->
        <router-link to="/produit"
          class="block bg-white rounded-xl shadow hover:shadow-lg hover:scale-105 transition duration-300 overflow-hidden">
          <img src="https://via.placeholder.com/300x200?text=Perle+Arc-en-ciel" alt="Perle Arc-en-ciel"
            class="w-full h-48 object-cover" />
          <div class="p-4 text-center">
            <h3 class="font-semibold text-lg text-gray-800">Perle Arc-en-ciel</h3>
            <p class="text-[#fc6b07] font-bold my-2">10,00€</p>
            <button class="bg-[#fc6b07] text-white px-4 py-1 rounded-full text-sm hover:bg-amber-700 transition">
              Voir le produit
            </button>
          </div>
        </router-link>
      </div>
    </div>
  </section>

  <!--Temoignage-->

  <section class="bg-white py-16 px-6 md:px-20">
    <div class="max-w-6xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-amber-700 mb-10">
        Ce que disent nos clientes
      </h2>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Témoignage 1 -->
        <div class=" p-6 hover:scale-105 transition duration-300">
          <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Client"
            class="w-16 h-16 rounded-full mx-auto mb-4" />
          <h3 class="font-semibold text-lg text-gray-800">Fatima B.</h3>
          <div class="flex justify-center mt-1 mb-3 text-amber-500">
            <span v-for="i in 5" :key="i">★</span>
          </div>
          <p class="text-gray-600 italic">
            "Magnifiques perles, très bonne qualité et livraison rapide. Je suis ravie de ma commande !"
          </p>
        </div>

        <!-- Témoignage 2 -->
        <div class=" p-6 hover:scale-105 transition duration-300">
          <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Client"
            class="w-16 h-16 rounded-full mx-auto mb-4" />
          <h3 class="font-semibold text-lg text-gray-800">Lina M.</h3>
          <div class="flex justify-center mt-1 mb-3 text-amber-500">
            <span v-for="i in 4" :key="i">★</span><span class="text-gray-300">★</span>
          </div>
          <p class="text-gray-600 italic">
            "Les couleurs sont superbes, je referai une commande sans hésiter."
          </p>
        </div>

        <!-- Témoignage 3 -->
        <div class=" p-6 hover:scale-105 transition duration-300">
          <img src="https://randomuser.me/api/portraits/women/12.jpg" alt="Client"
            class="w-16 h-16 rounded-full mx-auto mb-4" />
          <h3 class="font-semibold text-lg text-gray-800">Aïssatou D.</h3>
          <div class="flex justify-center mt-1 mb-3 text-amber-500">
            <span v-for="i in 5" :key="i">★</span>
          </div>
          <p class="text-gray-600 italic">
            "Dreams_Pearls m’a vraiment surprise, c’est encore plus beau en vrai qu’en photo !"
          </p>
        </div>
      </div>
    </div>
  </section>

  <!--Promo-->

  <section class="relative bg-amber-100 py-16 px-6 md:px-20 overflow-hidden">
    <!-- Fond décoratif -->
    <div
      class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1616077167185-58f92fa9a26d')] bg-cover bg-center opacity-10 pointer-events-none">
    </div>

    <div class="relative max-w-5xl mx-auto text-center">
      <h2 class="text-4xl md:text-5xl font-bold text-amber-800 mb-6">
        🎉 Offre Spéciale -20% sur vos perles préférées !
      </h2>
      <p class="text-gray-700 text-lg md:text-xl mb-8">
        Cette semaine seulement, profitez de 20% de réduction sur la collection "Perles Cristal". Faites briller vos
        créations
      </p>
      <router-link to="/produit"
        class="inline-block bg-amber-700 text-white px-6 py-3 rounded-full text-lg font-semibold hover:bg-amber-800 transition duration-300">
        Voir les produits
      </router-link>
    </div>
  </section>

  <section class="bg-white py-20 px-6 md:px-20">
    <div class="max-w-6xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-amber-700 mb-12">
        Pourquoi choisir <span class="italic">Dreams_Pearls</span> ?
      </h2>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-10">
        <!-- Bloc 1 -->
        <div class="flex flex-col items-center text-center p-4">
          <svg class="w-12 h-12 text-amber-600 mb-4" fill="none" stroke="currentColor" stroke-width="2"
            viewBox="0 0 24 24">
            <path d="M5 13l4 4L19 7" />
          </svg>
          <h3 class="font-semibold text-lg mb-2">Qualité supérieure</h3>
          <p class="text-gray-600 text-sm">Des perles sélectionnées avec soin, durables et éclatantes.</p>
        </div>

        <!-- Bloc 2 -->
        <div class="flex flex-col items-center text-center p-4">
          <svg class="w-12 h-12 text-amber-600 mb-4" fill="none" stroke="currentColor" stroke-width="2"
            viewBox="0 0 24 24">
            <path d="M12 8v4l3 3" />
            <path d="M12 22C6.48 22 2 17.52 2 12S6.48 2 12 2s10 4.48 10 10" />
          </svg>
          <h3 class="font-semibold text-lg mb-2">Livraison rapide</h3>
          <p class="text-gray-600 text-sm">Expédition en 48h partout en France et à l’international.</p>
        </div>

        <!-- Bloc 3 -->
        <div class="flex flex-col items-center text-center p-4">
          <svg class="w-12 h-12 text-amber-600 mb-4" fill="none" stroke="currentColor" stroke-width="2"
            viewBox="0 0 24 24">
            <path d="M12 2l9 4.5v11L12 22l-9-4.5v-11L12 2z" />
          </svg>
          <h3 class="font-semibold text-lg mb-2">Satisfait ou remboursé</h3>
          <p class="text-gray-600 text-sm">Retour facile sous 14 jours si le produit ne vous convient pas.</p>
        </div>

        <!-- Bloc 4 -->
        <div class="flex flex-col items-center text-center p-4">
          <svg class="w-12 h-12 text-amber-600 mb-4" fill="none" stroke="currentColor" stroke-width="2"
            viewBox="0 0 24 24">
            <path d="M12 14l9-5-9-5-9 5 9 5z" />
            <path d="M12 14l6.16-3.422A12.094 12.094 0 0112 21.5c-2.61 0-5.04-.837-7-2.25L12 14z" />
          </svg>
          <h3 class="font-semibold text-lg mb-2">Artisanat passionné</h3>
          <p class="text-gray-600 text-sm">Une entreprise locale portée par la passion des perles.</p>
        </div>
      </div>
    </div>
  </section>
  

  <!-- Map Google -->
    <div class="mt-20">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3965.305931116426!2d2.4351876758469317!3d6.3544284251032845!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x10235509a86a5ab5%3A0x284ff4b0eac477a7!2sVIPP%20Interstis%20Ganhi!5e0!3m2!1sfr!2sbj!4v1745585475520!5m2!1sfr!2sbj" width="100%" height="450" style="border:0;"
        allowfullscreen="" loading="lazy" class="rounded-lg shadow"></iframe>
    </div> 
</template>

<style scoped></style>