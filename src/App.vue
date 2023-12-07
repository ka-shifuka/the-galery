<!-- script -->
<script setup>
  import Images from "./components/Images.vue";
  import data from "./assets/data.json";
</script>
<!-- end script -->

<!-- template -->
<template>
  <section class="@Container min-h-screen flex flex-col justify-between">
    <!-- header and main content -->
    <div class="@wrap p-6">
      <header class="flex items-center gap-2">
        <!-- title and icon -->
        <img class="w-10 h-10 rounded-lg" src="/icon.jpg" />
        <div class="@wrap flex flex-col justify-center">
          <h1 class="relative top-1.5 font-semibold text-lg">The Galery</h1>
          <p class="text-[10px]">Create By Arya Dewangga Puja | ka-shifuka</p>
        </div>
        <!-- title and icon -->
      </header>

      <main class="mt-6 columns-1 sm:columns-2 md:columns-3">
        <div v-for="image in data">
          <images class="mb-6" :url="image.url"></images>
        </div>
      </main>
    </div>
    <!-- endheader and main content -->

    <!-- footer -->
    <div class="@wrap">footer</div>
    <!-- end footer -->
  </section>
</template>
<!-- end template -->

<!-- style -->
<style scoped></style>
<!-- end stayle -->
