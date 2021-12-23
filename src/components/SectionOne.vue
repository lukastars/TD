<template>
  <div
    class="px-9 sm:px-16 py-16 sm:py-32 pt-[8rem] flex section"
    id="section1"
  >
    <div class="flex flex-col sm:flex-row items-center border-b-2 pb-[8rem]">
      <div
        class="w-full md:w-[48%] mr-0 sm:mr-7 flex flex-col items-center pt-10 sm:pt-0"
      >
        <img src="../assets/hawaii.jpg" alt="" class="rounded-xl" />
      </div>
      <div
        class="w-full md:w-[52%] flex flex-col items-center sm:items-start order-first sm:order-last"
      >
        <h1 class="text-2xl lg:text-3xl font-bold font-serif mb-5">
          Section 1
        </h1>
        <div class="flex flex-col w-fit text-xs md:text-sm lg:text-lg">
          <div class="grid grid-cols-1 sm:grid-cols-4 mb-2 md:mb-4 lg:mb-6">
            <p class="text-[#585f65] col-span-1 font-bold">Population</p>
            <p class="col-span-3">Total (1,415,872), Rank (40th)</p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-4 mb-2 md:mb-4 lg:mb-6">
            <p class="text-[#585f65] col-span-1 font-bold">Dimensions</p>
            <p class="col-span-3">
              Length 1,522 mi (2,450 km), Width n/a mi (n/a km)
            </p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-4 mb-2 md:mb-4 lg:mb-6">
            <p class="text-[#585f65] col-span-1 font-bold">Language</p>
            <p class="col-span-3">Official languages English, Hawaiin</p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-4 mb-2 md:mb-4 lg:mb-6">
            <p class="text-[#585f65] col-span-1 font-bold">Largest city</p>
            <p class="col-span-3">The capital (Honolulu)</p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-4 mb-2 md:mb-4 lg:mb-6">
            <p class="text-[#585f65] col-span-1 font-bold">Largest metro</p>
            <p class="col-span-3">The Largest metro in Island of O'ahu</p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-4">
            <p class="text-[#585f65] col-span-1 font-bold">Elevation</p>
            <p class="col-span-3">Highest elevation 13,796 ft (4,205.0 m)</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionOne',
};
</script>

<style></style>
