<template>
  <div
    id="main"
    class="flex justify-center items-center mt-20 font-['Poppins'] gap-20"
  >
    <div
      id="left"
      class="w-[40%] flex flex-col justify-center items-center gap-10"
    >
      <h1 class="font-semibold text-[48px]">Biz bilan o'rganishni boshlang!</h1>
      <h3 class="text-[20px] text-[#8a8a8a]">
        Bizdan tajribali o'qituvchilar, sinalgan o'quv dasturi va doimiy
        repetitsion testlar - sizdan esa qat'iy nazorat va o'z vaqtida qilingan
        to'lovlar😉, qarabsizki farzandingiz o'qishga kirishga tayyor!
      </h3>
    </div>
    <img src="/bestway.jpg" alt="Start" class="rounded-md w-[500px]" />
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@media screen and (max-width: 1000px) {
  img {
    width: 400px;
  }
}

@media screen and (max-width: 800px) {
  img {
    width: 300px;
    height: 300px;
  }
}

@media screen and (max-width: 700px) {
  #main {
    gap: 20px;
  }
  #left {
    h1 {
      font-size: 30px;
    }
    h3 {
      font-size: 16px;
    }
  }
}

@media screen and (max-width: 600px) {
  img {
    width: 200px;
    height: 200px;
  }
  #left {
    h1 {
      font-size: 24px;
    }
    h3 {
      font-size: 12px;
    }
  }
}

@media screen and (max-width: 450px) {
  #left {
    gap: 10px;
  }
  img {
    width: 150px;
    height: 150px;
  }
}
</style>
