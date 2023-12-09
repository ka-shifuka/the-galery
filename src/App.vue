<!-- script -->
<script setup>
  import Images from "./components/Images.vue";
  import data from "./assets/data.json";
</script>
<!-- end script -->

<!-- template -->
<template>
  <section class="@Container flex flex-col justify-between">
    <!-- header and main content -->
    <div class="@wrap p-6">
      <header class="flex items-center justify-between select-none">
        <!-- title and icon -->
        <div class="@wrap flex items-center gap-2">
          <div
            class="w-10 h-10 rounded-lg bg-cover"
            style="background-image: url(&quot;/icon.jpg&quot;)"
          ></div>
          <div class="@wrap flex flex-col justify-center">
            <h1 class="h-6 font-semibold text-lg">The Galery</h1>
            <p class="text-[10px]">Create By Arya Dewangga Puja | ka-shifuka</p>
          </div>
          <!-- title and icon -->
        </div>

        <div class="@wrap w-10 h-10 flex items-center justify-end">
          <!-- github link -->
          <a
            class="text-2xl cursor-pointer"
            href="https://github.com/ka-shifuka/the-galery"
          >
            <i class="bi bi-github"></i>
          </a>
          <!-- github link -->
        </div>
      </header>

      <main
        class="mt-6 gap-10 columns-1 sm:columns-2 md:columns-3 lg:columns-4"
      >
        <images v-for="image in data" class="mb-10" :url="image"></images>
      </main>
    </div>
    <!-- endheader and main content -->

    <!-- footer -->
    <div class="@wrap">
      <footer
        class="w-full h-32 flex flex-col items-center justify-center select-none"
      >
        <h1 class="font-semibold text-md">----- End of Galery -----</h1>
        <p class="text-[12px] text-zinc-700">
          &copy;Arya Dewangga Puja | ka-shifuka
        </p>
      </footer>
    </div>
    <!-- end footer -->
  </section>
</template>
<!-- end template -->

<!-- style -->
<style scoped></style>
<!-- end stayle -->
