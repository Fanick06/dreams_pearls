<script setup>

import { ref } from 'vue'

const categories = ['bracelet', 'collier', 'bayas']
const categorieActive = ref('bracelet')

const produits = {
  bracelet: [
    { id: 1, nom: 'Bracelet Océan', prix: 14.9, image: 'https://source.unsplash.com/400x300/?bracelet', badge: 'Nouveau' },
    { id: 2, nom: 'Bracelet Soleil', prix: 13.5, image: 'https://source.unsplash.com/400x300/?jewelry', badge: 'Promo' },
    { id: 3, nom: 'Bracelet Nature', prix: 12.0, image: 'https://source.unsplash.com/400x300/?beads' },
    { id: 4, nom: 'Bracelet Bleu', prix: 15.0, image: 'https://source.unsplash.com/400x300/?fashion' },
    { id: 5, nom: 'Bracelet Ambre', prix: 18.0, image: 'https://source.unsplash.com/400x300/?stone' },
    { id: 6, nom: 'Bracelet Quartz', prix: 19.9, image: 'https://source.unsplash.com/400x300/?gem' },
    { id: 7, nom: 'Bracelet Terre', prix: 12.5, image: 'https://source.unsplash.com/400x300/?natural' },
    { id: 8, nom: 'Bracelet Doux', prix: 11.9, image: 'https://source.unsplash.com/400x300/?handmade' },
  ],
  collier: [
    { id: 9, nom: 'Collier Lune', prix: 22.9, image: 'https://source.unsplash.com/400x300/?necklace', badge: 'Nouveau' },
    { id: 10, nom: 'Collier Émeraude', prix: 25.0, image: 'https://source.unsplash.com/400x300/?emerald' },
    { id: 11, nom: 'Collier Cristal', prix: 28.9, image: 'https://source.unsplash.com/400x300/?crystal' },
    { id: 12, nom: 'Collier Perle Blanche', prix: 30.0, image: 'https://source.unsplash.com/400x300/?pearl' },
    { id: 13, nom: 'Collier Nuit', prix: 21.0, image: 'https://source.unsplash.com/400x300/?luxury', badge: 'Promo' },
    { id: 14, nom: 'Collier Douceur', prix: 23.5, image: 'https://source.unsplash.com/400x300/?jewel' },
    { id: 15, nom: 'Collier Élégance', prix: 27.0, image: 'https://source.unsplash.com/400x300/?elegance' },
    { id: 16, nom: 'Collier Nature', prix: 24.0, image: 'https://source.unsplash.com/400x300/?nature' },
  ],
  bayas: [
    { id: 17, nom: 'Bayas Dorée', prix: 8.9, image: '/assets/pi.jpg', badge: 'Promo' },
    { id: 18, nom: 'Bayas Colorée', prix: 9.5, image: '/assets/mp.jpg', badge: 'Nouveau' },
    { id: 19, nom: 'Bayas Pure', prix: 10.0, image: '/assets/tui.webp' },
    { id: 20, nom: 'Bayas Verre', prix: 9.9, image: 'https://source.unsplash.com/400x300/?glass' },
    { id: 21, nom: 'Bayas Pastel', prix: 11.0, image: 'https://source.unsplash.com/400x300/?pastel' },
    { id: 22, nom: 'Bayas Naturelle', prix: 8.5, image: 'https://source.unsplash.com/400x300/?stone' },
    { id: 23, nom: 'Bayas Fantaisie', prix: 10.9, image: 'https://source.unsplash.com/400x300/?art' },
    { id: 24, nom: 'Bayas Éclat', prix: 7.5, image: 'https://source.unsplash.com/400x300/?shine' },
  ],
  
}

</script>

<template>
  

  
<section class="px-4 py-12 md:px-16 bg-white text-gray-800">
    <!-- Titre -->
    <div class="text-center mb-10">
      <h1 class="text-3xl md:text-4xl font-bold text-amber-600">Nos Collections de Perles</h1>
      <p class="text-gray-600 mt-2">Explorez notre collection de perles artisanales uniques et éclatantes</p>
    </div>

    <!-- Boutons de catégories -->
    <div class="flex flex-wrap justify-center gap-4 mb-12">
      <button
        v-for="categorie in categories"
        :key="categorie"
        @click="categorieActive = categorie"
        :class="[
          'px-5 py-2 rounded-full text-sm font-semibold transition duration-300',
          categorieActive === categorie
            ? 'bg-amber-600 text-white shadow-md'
            : 'bg-gray-100 text-amber-800 hover:bg-amber-200'
        ]"
      >
        {{ categorie }}
      </button>
    </div>

    <!-- Grille de produits -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
      <div
        v-for="produit in produits[categorieActive]"
        :key="produit.id"
        class="bg-amber-50 rounded-xl shadow hover:shadow-lg hover:scale-105 transition-all duration-300 overflow-hidden relative"
      >
        <!-- Badge si dispo -->
        <span
          v-if="produit.badge"
          class="absolute top-2 left-2 bg-red-500 text-white text-xs px-2 py-1 rounded shadow"
        >
          {{ produit.badge }}
        </span>

        <!-- Image -->
        <router-link :to="`/produit/${produit.id}`">
          <img :src="produit.image" :alt="produit.nom" class="w-full h-48 object-cover" />
        </router-link>

        <!-- Détails produit -->
        <div class="p-4">
          <h3 class="text-lg font-bold text-amber-800">{{ produit.nom }}</h3>
          <p class="text-gray-600">{{ produit.prix }} €</p>

          <router-link
            to="/panier"
            class="inline-block mt-3 bg-amber-600 text-white text-sm px-4 py-2 rounded-full hover:bg-amber-700 transition"
          >
            Ajouter au panier
          </router-link>
        </div>
      </div>
    </div>
  </section>
    
</template>

<style scoped></style>