<!-- script -->
<script setup>
  import Images from "./components/Images.vue";
</script>
<!-- end script -->

<!-- template -->
<template>
  <!-- height ground -->
  <div
    class="w-[200vh] -top-20 -left-20 h-20 absolute bg-black blur-xl -z-50"
  ></div>
  <!-- end height ground -->

  <section class="@Container min-h-screen flex flex-col justify-between">
    <!-- header and main content -->
    <div class="@wrap p-6 flex flex-col gap-6">
      header main
      <Images
        textwhite
        title="Ryo yamada"
        description="dolore tempor exercitation reprehenderit cupidatat nostrud enim mollit ullamco dolore nulla deserunt laborum veniam reprehenderit et nostrud pariatur sint velit"
        url="/pictures/images_1.jpeg"
      ></Images>
      <Images
        textwhite
        title="Ryo yamada"
        description="dolore tempor exercitation reprehenderit cupidatat nostrud enim mollit ullamco dolore nulla deserunt laborum veniam reprehenderit et nostrud pariatur sint velit"
        url="/pictures/images_2.jpeg"
      ></Images>
      <Images
        textwhite
        title="Ryo yamada"
        description="dolore tempor exercitation reprehenderit cupidatat nostrud enim mollit ullamco dolore nulla deserunt laborum veniam reprehenderit et nostrud pariatur sint velit"
        url="/pictures/images_3.jpeg"
      ></Images>
      <Images
        textwhite
        title="Ryo yamada"
        description="dolore tempor exercitation reprehenderit cupidatat nostrud enim mollit ullamco dolore nulla deserunt laborum veniam reprehenderit et nostrud pariatur sint velit"
        url="/pictures/images_4.jpeg"
      ></Images>
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
