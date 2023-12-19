<!-- script -->
<script setup>
  /*
   * Define properties in this component
   * url : url of images
   */
  const props = defineProps({
    url: String
  });
</script>
<!-- end script -->

<!-- template -->
<template>
  <div class="@wrap w-full min-h-[10rem] rounded-xl relative group">
    <figure>
      <!-- main image -->
      <div
        class="group-hover:scale-105 duration-[400ms] group-hover:-translate-y-4"
      >
        <img
          class="w-full h-fit rounded-xl transition-all"
          :src="props.url"
          loading="lazy"
          alt="pictures"
        />

        <!-- download link -->
        <a
          download
          class="absolute bottom-1.5 right-1.5 p-2 text-xs text-zinc-100 rounded-md backdrop-blur cursor-pointer"
          :href="props.url"
        >
          <i class="bi bi-arrow-down"></i> Download
        </a>
        <!-- end download link -->
      </div>
      <!-- end  main image -->

      <!-- background to create blur effect -->
      <img
        class="w-full h-fit rounded-xl blur-md absolute top-4 right-0 -z-10 brightness-75 transition-all duration-[400ms] group-hover:scale-95 group-hover:-translate-y-2"
        :src="props.url"
        loading="lazy"
        alt="pictures blur effect"
      />
      <!-- end background to create blur effect -->
    </figure>
  </div>
</template>
<!-- end template -->

<!-- style -->
<style scoped></style>
<!-- end stayle -->
