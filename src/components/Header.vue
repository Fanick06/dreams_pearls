<script setup>
import { RouterLink } from 'vue-router'
import { HomeIcon, ShoppingCartIcon } from '@heroicons/vue/24/outline'
</script>

<template>
    <header>

        <nav class="bg-white shadow-xl border-b-4 border-amber-600 px-6 py-1 flex justify-around items-center text-gray-800 text-lg font-medium">
        
            <div class="flex flex-col items-start">
                <img class="h-[100px] w-[100px]" src="../assets/Dreams_Pearls.png" alt="">
            </div>
            <div class="flex gap-4 justify-center">
                <router-link to="/" class="hover:text-[#fc6b07] transition">Accueil</router-link>
                <router-link to="/about" class="hover:text-[#fc6b07] transition">À propos</router-link>
                <router-link to="/produit" class="hover:text-[#fc6b07] transition">Produit</router-link>
                <router-link to="/contact" class="hover:text-[#fc6b07] transition">Contact</router-link>
            </div>

            <div class="">
                <router-link to="/panier" class="hover:text-[#fc6b07] transition">Panier 🛒</router-link>
            </div>

        </nav>
    </header>

    <!-- <RouterView /> -->
</template>

<style scoped></style>