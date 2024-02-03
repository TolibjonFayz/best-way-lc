<template>
  <div id="main" class="mt-28 font-['Poppins']">
    <h1 id="why" class="font-semibold text-[40px] ml-40">
      Nima uchun “Best Way”da o‘qish kerak?
    </h1>
    <div id="whys" class="flex justify-center mt-10 gap-10">
      <div class="flex flex-col gap-5 w-[40%] p-10 bg-[#F3F8FF] rounded-3xl">
        <img src="/spark.png" alt="Sifatli ta'lim" class="w-[50px]" />
        <h1 class="text-[24px] font-semibold">Sifatli ta'lim</h1>
        <h3 class="text-[#667085] text-[18px] font-medium">
          Doimiy yangilanib boradigan kurslar va katta tajribaga ega ustozlar.
        </h3>
      </div>

      <div class="flex flex-col gap-5 w-[40%] p-10 bg-[#F3F8FF] rounded-3xl">
        <img src="/office-building.png" alt="Sifatli ta'lim" class="w-[50px]" />
        <h1 class="text-[24px] font-semibold">Zamonaviy ofis</h1>
        <h3 class="text-[#667085] text-[18px] font-medium">
          Zamonaviy qulayliklarga ega sinf xonalar.
        </h3>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@media screen and (max-width: 800px) {
  #why {
    margin-left: 50px;
  }
}

@media screen and (max-width: 600px) {
  #why {
    margin-left: 30px;
    font-size: 24px;
    margin-right: 20px;
  }
  #whys {
    flex-direction: column;
    align-items: center;
  }
  #whys div {
    width: 90%;
  }
}
</style>
