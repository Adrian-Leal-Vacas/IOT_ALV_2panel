<script setup>
import lookCollection from './components/lookCollection.vue'
</script>
<template>
  <div class="w-auto m-2.5">
    <nav class="bg-blue-500 text-white p-2.5 w-full flex justify-between items-center">
      <p id="logo" class="no-underline text-white font-bold text-3xl">
        IOT_ALV <span class="text-base">2panel</span>
      </p>
    </nav>
    <lookCollection />
  </div>
  <div class="w-auto m-2.5">
    <footer class="bg-blue-500 text-white p-2.5 flex justify-center items-center">
      <p>
        &copy; 2024 IOT_ALV Realizado por
        <a
          class="font-bold text-rose-800 hover:text-sky-900"
          href="https://adrian-leal-vacas.github.io/"
          target="_blank"
          rel="noopener noreferrer"
          >Adrián Leal Vacas</a
        >
      </p>
    </footer>
  </div>
</template>
<style lang="scss" scoped></style>
