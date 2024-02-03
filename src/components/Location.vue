<template>
  <div id="contact" class="mt-28 font-['Poppins']">
    <h1 id="title" class="ml-32 font-semibold text-[40px] mb-8">
      Bizning manzil
    </h1>
    <div id="in" class="flex justify-center gap-8">
      <iframe
        class="rounded-xl"
        src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d1525.4341270214709!2d64.4895026!3d40.1229394!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3f507af2c984c7cb%3A0xf735c24c46dfd29d!2sBest%20Way%20Tutoring!5e0!3m2!1sen!2s!4v1706894250790!5m2!1sen!2s"
        width="800"
        height="600"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>

      <div id="info" class="w-[30%] p-5 rounded-xl flex flex-col gap-5">
        <h1 class="text-[24px] font-medium">Buxoro, Shofirkon</h1>
        <img src="/bestway.png" alt="Logo" />
        <h2 id="location" class="pb-5">Markaziy Savrak mahallasi 10-uy</h2>
        <div>
          <h1 class="text-[#667085] text-[20px]">Mo'ljal</h1>
          <h2 id="location" class="pb-5">Bisyor kafe</h2>
        </div>
        <div>
          <h1 class="text-[#667085] text-[20px]">Telefon</h1>
          <h2 class="">+998 99 558 84 06</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
#info {
  border: 1px solid #eaecf0;
}
#location {
  border-bottom: 1px solid #eaecf0;
}
@media screen and (max-width: 1000px) {
  #in {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  #title {
    margin-left: 30px;
  }
  #info {
    width: 90%;
  }
}

@media screen and (max-width: 820px) {
  iframe {
    width: 90%;
  }
}
</style>
