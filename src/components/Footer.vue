<template>
  <div
    id="main"
    class="flex justify-between mt-20 pt-14 pb-14 pl-40 pr-40 bg-[#F9FAFB] font-['Poppins']"
  >
    <div
      id="rightmini"
      class="hidden text-[#98A2B3] flex-col items-center justify-center gap-3"
    >
      <div id="socials" class="text-[#98A2B3] flex gap-8 text-[24px]">
        <a href="https://t.me/best_way_shafirkan" target="_blank">
          <i class="fa-brands fa-telegram"></i>
        </a>

        <a
          href="https://www.instagram.com/best_way_education?igsh=YmVwYmtnamk5enp1"
          target="_blank"
        >
          <i class="fa-brands fa-square-instagram"></i>
        </a>

        <a
          href="https://youtube.com/@azizakhtamov22485?si=1Aqaoze-wxb4hQWm"
          target="_blank"
        >
          <i class="fa-brands fa-youtube"></i>
        </a>

        <a
          href="https://www.linkedin.com/in/aziz-akhtamov-0bb458121?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"
          target="_blank"
        >
          <i class="fa-brands fa-linkedin"></i>
        </a>

        <a
          href="https://www.facebook.com/aakhtamov?mibextid=ZbWKwL"
          target="_blank"
        >
          <i class="fa-brands fa-facebook"></i>
        </a>
      </div>

      <div class="flex items-center">
        <h4>Aloqa</h4>
        <h1 class="text-[20px] font-medium text-[#667085]">
          &nbsp;&nbsp;&nbsp;+998 99 558 84 06
        </h1>
      </div>
    </div>

    <div id="left" class="flex items-center gap-10">
      <img src="/logo.png" alt="Logo" class="w-[80px] rounded-3xl" />
      <h1 class="text-[#98A2B3]">
        © “Best Way”, 2024 - Barcha huquqlar himoyalangan.
      </h1>
    </div>

    <div
      id="right"
      class="text-[#98A2B3] flex flex-col items-center justify-center gap-3"
    >
      <div id="socials" class="text-[#98A2B3] flex gap-8 text-[24px]">
        <a href="https://t.me/best_way_shafirkan" target="_blank">
          <i class="fa-brands fa-telegram"></i>
        </a>

        <a
          href="https://www.instagram.com/best_way_education?igsh=YmVwYmtnamk5enp1"
          target="_blank"
        >
          <i class="fa-brands fa-square-instagram"></i>
        </a>

        <a
          href="https://youtube.com/@azizakhtamov22485?si=1Aqaoze-wxb4hQWm"
          target="_blank"
        >
          <i class="fa-brands fa-youtube"></i>
        </a>

        <a
          href="https://www.linkedin.com/in/aziz-akhtamov-0bb458121?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"
          target="_blank"
        >
          <i class="fa-brands fa-linkedin"></i>
        </a>

        <a
          href="https://www.facebook.com/aakhtamov?mibextid=ZbWKwL"
          target="_blank"
        >
          <i class="fa-brands fa-facebook"></i>
        </a>
      </div>

      <div class="flex items-center">
        <h4>Aloqa</h4>
        <h1 class="text-[20px] font-medium text-[#667085]">
          &nbsp;&nbsp;&nbsp;+998 99 558 84 06
        </h1>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@media screen and (max-width: 1000px) {
  #main {
    padding-left: 50px;
    padding-right: 50px;
  }
}

@media screen and (max-width: 900px) {
  #main {
    flex-direction: column;
    flex-wrap: wrap;
    padding-left: 40px;
    padding-right: 40px;
    justify-content: centers;
    align-items: center;
  }
  #right {
    display: none;
  }
  #rightmini {
    display: flex;
  }
}

@media screen and (max-width: 530px) {
  #main {
    padding-left: 20px;
    padding-right: 20px;
  }
}
</style>
