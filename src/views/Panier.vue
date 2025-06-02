<script setup>
import { ref, computed } from 'vue'


const panier = ref([
  {
    id: 1,
    nom: 'Bracelet Océan',
    prix: 14.9,
    image: 'https://source.unsplash.com/400x300/?bracelet',
    quantite: 2,
  },
  {
    id: 9,
    nom: 'Collier Lune',
    prix: 22.9,
    image: 'https://source.unsplash.com/400x300/?necklace',
    quantite: 1,
  },
])

// Supprimer un produit du panier
function retirerDuPanier(index) {
  panier.value.splice(index, 1)
}

// Total général
const totalPanier = computed(() =>
  panier.value.reduce((total, item) => total + item.prix * item.quantite, 0)
)
</script>

<template>

    <section class="min-h-screen px-4 py-12 md:px-16 bg-white text-gray-800">
    <h1 class="text-3xl font-bold text-amber-700 mb-6">Votre Panier</h1>

    <!-- Si panier vide -->
    <div v-if="panier.length === 0" class="text-gray-600">
      Votre panier est vide.
      <router-link to="/produit" class="text-amber-600 underline ml-2">Voir les produits</router-link>
    </div>

    <!-- Si panier avec produits -->
    <div v-else class="space-y-6">
      <div
        v-for="(item, index) in panier"
        :key="item.id"
        class="flex items-center justify-between bg-amber-50 rounded-lg p-4 shadow"
      >
        <!-- Image -->
        <img :src="item.image" alt="Produit" class="w-20 h-20 object-cover rounded-md" />

        <!-- Détails -->
        <div class="flex-1 px-4">
          <h3 class="font-semibold text-lg">{{ item.nom }}</h3>
          <p class="text-sm text-gray-600">Prix unitaire : {{ item.prix }} €</p>
          <p class="text-sm text-gray-600">Quantité : {{ item.quantite }}</p>
        </div>

        <!-- Total + Supprimer -->
        <div class="text-right">
          <p class="text-amber-800 font-bold mb-2">
            Total : {{ (item.prix * item.quantite).toFixed(2) }} €
          </p>
          <button
            @click="retirerDuPanier(index)"
            class="text-sm text-red-500 hover:underline"
          >
            Supprimer
          </button>
        </div>
      </div>

      <!-- Total général -->
      <div class="text-right text-xl font-bold text-amber-800 mt-4">
        Total à payer : {{ totalPanier.toFixed(2) }} €
      </div>
    </div>
  </section>


    <!-- <div class="p-6">
        <h2 class="text-2xl font-semibold mb-6">Votre panier</h2>
        <p class="text-gray-500">Votre panier est vide pour le moment.</p>
    </div> -->
</template>

<style scoped></style>