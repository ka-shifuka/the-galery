<!-- script -->
<script setup>
  import { ref, onMounted } from "vue";

  const slideActive = ref(false); // slide is to show figcaption
  /*
   * Define properties in this component
   * url : url of images
   * title : figure title
   * description : figure description
   * bgcolor : figcaption background color
   * textwhite : use if the background is dark
   */
  const props = defineProps({
    url: String,
    title: String,
    description: String,
    bgcolor: { type: String, default: "#D8C8BB" },
    textwhite: Boolean
  });

  /*
   * if is scroll slideActive become false
   */
  onMounted(() => {
    window.addEventListener("scroll", function () {
      slideActive.value = false;
    });
  });
</script>
<!-- end script -->

<!-- template -->
<template>
  <div class="@wrap w-fit h-fit relative">
    <figure>
      <!-- main image -->
      <img
        class="w-full h-fit rounded-xl"
        :src="props.url"
        alt="pictures"
        @mouseover="slideActive = false"
      />
      <!-- end  main image -->

      <!-- background to create blur effect -->
      <img
        class="w-full h-fit rounded-xl blur-md absolute top-4 right-0 -z-10"
        :src="props.url"
        alt="pictures"
      />
      <!-- end background to create blur effect -->

      <!-- download link -->
      <a
        class="absolute bottom-1.5 right-1.5 p-2 bg-transparent backdrop-blur-2xl text-[12px] text-zinc-100 rounded-md"
        :href="props.url"
        download
      >
        <i class="bi bi-arrow-down"></i> Download
      </a>
      <!-- end download link -->

      <!-- counter slideActive -->
      <button
        @click="slideActive = !slideActive"
        class="absolute w-fit h-fit bottom-1.5 left-1.5 py-2 px-3 bg-transparent backdrop-blur-2xl text-[12px] text-zinc-100 rounded-md"
      >
        <i class="bi bi-card-text"></i>
      </button>
      <!-- counter slideActive -->
    </figure>

    <figcaption
      class="absolute h-full top-0 left-0 transition-all duration-300 overflow-hidden"
      :class="slideActive ? 'w-full' : 'w-0'"
    >
      <div
        class="@wrap h-full w-2/3 min-w-[150px] p-3 rounded-xl z-10"
        :class="props.textwhite ? 'text-zinc-100' : 'text-zinc-900'"
        :style="`background-color: ${bgcolor}`"
      >
        <div class="@wrap flex justify-between">
          <h1 class="text-md font-semibold">{{ props.title }}</h1>

          <!-- counter slideActive -->
          <button @click="slideActive = !slideActive" class="text-md">
            <i class="bi bi-x"></i>
          </button>
          <!-- end counter slideActive -->
        </div>
        <p class="text-sm">{{ props.description }}</p>
      </div>
    </figcaption>
  </div>
</template>
<!-- end template -->

<!-- style -->
<style scoped></style>
<!-- end stayle -->
