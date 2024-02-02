<template>
  <div
    id="main"
    class="flex items-center justify-between font-['Poppins'] pl-40 pr-40 pt-5 pb-5"
  >
    <div id="logo" class="flex items-center gap-3">
      <img src="/logo.png" alt="Logo" class="w-[60px] rounded-full" />
      <h1 class="text-[25px]">Best Way LC</h1>
    </div>
    <div id="navs" class="flex gap-8 text-[#444]">
      <a href="#main" class="hover:text-black">Asosiy menu</a>
      <a href="#about" class="hover:text-black">Biz haqimizda</a>
      <a href="#teachers" class="hover:text-black">O'qituvchilar</a>
      <a href="#courses" class="hover:text-black">Kurslar</a>
      <a href="#contact" class="hover:text-black">Aloqa</a>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
#main {
  border-bottom: 1px solid #eaecf0;
}
#navs {
  a {
    transition: all ease-in-out 0.1s;
  }
}
@media screen and (max-width: 1000px) {
  #main {
    padding-left: 40px;
    padding-right: 40px;
  }
}

@media screen and (max-width: 800px) {
  #main {
    text-align: center;
    flex-direction: column;
    padding-left: 20px;
    padding-right: 20px;
  }
}

@media screen and (max-width: 552px) {
  #navs a {
    font-size: 12px;
  }
  #navs {
    gap: 15px;
    align-items: center;
  }
  #main {
    padding-left: 15px;
    padding-right: 15px;
  }
}
</style>
