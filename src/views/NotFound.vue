<script setup>

</script>

<template>
    <section class="min-h-screen flex flex-col items-center justify-center bg-amber-50 text-center px-4">
        <!-- Code 404 -->
        <h1 class="text-8xl font-extrabold text-amber-600 mb-4">404</h1>

        <!-- Message -->
        <h2 class="text-2xl font-semibold text-gray-800 mb-2">Page non trouvée</h2>
        <p class="text-gray-600 max-w-md mb-6">
            Désolé, la page que vous recherchez n'existe pas ou a été déplacée.
        </p>

        <!-- Bouton vers Accueil -->
        <router-link to="/"
            class="bg-amber-600 text-white px-6 py-3 rounded-lg shadow hover:bg-amber-700 transition duration-300">
            Retour à l'accueil
        </router-link>
    </section>
</template>

<style scoped></style>