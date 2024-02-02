<template>
  <div id="main" class="mt-20 font-['Poppins']">
    <h1 id="title" class="font-semibold text-[40px] ml-40">Kurslar</h1>
    <div
      id="courses"
      class="flex flex-wrap justify-center gap-5 mt-10 ml-10 mr-10"
    >
      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[28%]"
      >
        <img src="/ielts.webp" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">President maktabi guruhi</h1>
          <h3 class="text-[#667085]">10 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img
          src="/cefrpng.png"
          alt="IELTS"
          class="w-[80px] h-[80px] rounded-full"
        />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Multilevel (CEFR)</h1>
          <h3 class="text-[#667085]">6 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/english.jpg" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Ingliz tili grammatikasi</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[28%]"
      >
        <img src="/ielts.webp" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">IELTS</h1>
          <h3 class="text-[#667085]">6 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/math.png" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Matematika</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/ona.jpg" alt="IELTS" class="w-[80px] h-[80px] rounded-xl" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Ona tili va Adabiyoti</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[28%]"
      >
        <img src="/history.png" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Tarix va Huquq</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/arab.png" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Arab tili</h1>
          <h3 class="text-[#667085]">6 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/rus.png" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Rus tili</h1>
          <h3 class="text-[#667085]">6 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[28%]"
      >
        <img
          src="/kimyo.png"
          alt="IELTS"
          class="w-[80px] h-[80px] rounded-full"
        />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Kimyo</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/biology.png" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Biologoya</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>

      <div
        class="course flex p-8 bg-[#F3F8FF] rounded-3xl gap-3 font-medium w-[27%]"
      >
        <img src="/physics.webp" alt="IELTS" class="w-[80px] h-[80px]" />
        <div class="in flex flex-col">
          <h1 class="text-[30px]">Fizika</h1>
          <h3 class="text-[#667085]">9 oy</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@media screen and (max-width: 1000px) {
  .course {
    width: 45%;
  }
  #title {
    margin-left: 70px;
  }
}

@media screen and (max-width: 850px) {
  .course {
    width: 80%;
  }
  #title {
    margin-left: 100px;
  }
}

@media screen and (max-width: 600px) {
  #courses {
    margin-left: 20px;
    margin-right: 20px;
  }
  .course {
    width: 95%;
  }
  #title {
    margin-left: 50px;
  }
}

@media screen and (max-width: 470px) {
  .course {
    width: 100%;
    h1 {
      font-size: 24px;
    }
  }
  #title {
    margin-left: 50px;
  }
}
</style>
