<!-- script -->
<script setup>
  import Images from "./components/Images.vue";
</script>
<!-- end script -->

<!-- template -->
<template>
  <section class="@Container min-h-screen flex flex-col justify-between">
    <!-- header and main content -->
    <div class="@wrap p-6 flex flex-col gap-6">
      header main
      <Images url="/pictures/images_1.jpeg"></Images>
      <Images url="/pictures/images_2.jpeg"></Images>
      <Images url="/pictures/images_3.jpeg"></Images>
      <Images url="/pictures/images_4.jpeg"></Images>
      <Images url="/pictures/images_5.jpeg"></Images>
      <Images url="/pictures/images_6.jpeg"></Images>
      <Images url="/pictures/images_7.jpeg"></Images>
      <Images url="/pictures/images_8.jpeg"></Images>
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
