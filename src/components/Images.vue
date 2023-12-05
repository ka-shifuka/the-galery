<!-- script -->
<script setup>
  const props = defineProps({
    url: String
  });
</script>
<!-- end script -->

<!-- template -->
<template>
  <div class="@wrap w-fit h-fit relative">
    <img class="w-full h-fit rounded-xl" :src="props.url" alt="pictures" />
    <img
      class="w-full h-fit rounded-xl blur-md absolute top-4 right-0 -z-10"
      :src="props.url"
      alt="pictures"
    />
    <a
      class="absolute bottom-1 right-1 p-2 bg-[rgba(0,0,0,0)] backdrop-blur-2xl text-[12px] text-zinc-100 rounded-md"
      download
      href="props.url"
    >
      <i class="bi bi-arrow-down"></i> Download
    </a>
  </div>
</template>
<!-- end template -->

<!-- style -->
<style scoped></style>
<!-- end stayle -->
