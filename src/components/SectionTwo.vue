<template>
  <div class="px-16 pt-[8rem] section" id="section2">
    <h1 class="text-3xl font-bold font-serif mb-5">Section 2</h1>
    <div class="border-b-2 pb-[8rem]">
      <div class="border-l-2 pl-5 pb-3">
        <div
          class="flex items-center pb-6 cursor-pointer"
          v-on:click="toggle('year1')"
        >
          <i
            class=""
            :class="[
              year1
                ? 'far fa-dot-circle text-xl absolute left-[3.4rem] text-[#044D73]'
                : 'fas fa-circle text-[0.5rem] absolute left-[3.78rem] text-gray-400',
            ]"
          ></i>
          <h1
            class=""
            :class="[
              year1 ? 'text-6xl' : 'text-4xl',
              'text-[#044D73]  font-bold font-serif ',
            ]"
          >
            1778
          </h1>
          <div class="w-[12rem]">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              :class="[year1 ? 'hidden' : '', 'h-12 w-[5rem] text-[#044D73]']"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 8l4 4m0 0l-4 4m4-4H3"
              />
            </svg>
          </div>
        </div>
        <p :class="[year1 ? '' : 'hidden', 'font-semibold']">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis
          earum ea libero ex laudantium non modi consectetur dolore reiciendis
          eaque. Officia sint autem quia quisquam ab porro at sunt omnis
          voluptatibus nihil! Provident, nam! Delectus.
        </p>
      </div>
      <div class="border-l-2 pl-5 pb-3">
        <div
          class="flex items-center pb-6 cursor-pointer"
          v-on:click="toggle('year2')"
        >
          <i
            class=""
            :class="[
              year2
                ? 'far fa-dot-circle text-xl absolute left-[3.4rem] text-[#044D73]'
                : 'fas fa-circle text-[0.5rem] absolute left-[3.78rem] text-gray-400',
            ]"
          ></i>
          <h1
            class=""
            :class="[
              year2 ? 'text-6xl' : 'text-4xl',
              'text-[#044D73]  font-bold font-serif ',
            ]"
          >
            1779
          </h1>
          <div class="w-[12rem]">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              :class="[year2 ? 'hidden' : '', 'h-12 w-[5rem] text-[#044D73]']"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 8l4 4m0 0l-4 4m4-4H3"
              />
            </svg>
          </div>
        </div>
        <p :class="[year2 ? '' : 'hidden', 'font-semibold']">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eos
          necessitatibus minima totam eaque sint quisquam quia obcaecati esse
          aliquam? Velit explicabo, sunt veniam nemo aspernatur laborum magnam
          dolorem labore esse. Iusto sunt architecto officia quia?
        </p>
      </div>
      <div class="border-l-2 pl-5 pb-3">
        <div
          class="flex items-center pb-6 cursor-pointer"
          v-on:click="toggle('year3')"
        >
          <i
            class=""
            :class="[
              year3
                ? 'far fa-dot-circle text-xl absolute left-[3.4rem] text-[#044D73]'
                : 'fas fa-circle text-[0.5rem] absolute left-[3.78rem] text-gray-400',
            ]"
          ></i>
          <h1
            class=""
            :class="[
              year3 ? 'text-6xl' : 'text-4xl',
              'text-[#044D73]  font-bold font-serif ',
            ]"
          >
            1789
          </h1>
          <div class="w-[12rem]">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              :class="[year3 ? 'hidden' : '', 'h-12 w-[5rem] text-[#044D73]']"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 8l4 4m0 0l-4 4m4-4H3"
              />
            </svg>
          </div>
        </div>
        <p :class="[year3 ? '' : 'hidden', 'font-semibold']">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse sapiente
          reiciendis consequatur, magni error velit assumenda tempora quam?
          Corporis aliquam similique officiis doloremque molestias nesciunt,
          totam maiores quod minus consectetur non ipsa necessitatibus
          cupiditate aliquid tempore dolor, ullam possimus quia.
        </p>
      </div>
      <div class="border-l-2 pl-5 pb-3">
        <div
          class="flex items-center pb-6 cursor-pointer"
          v-on:click="toggle('year4')"
        >
          <i
            class=""
            :class="[
              year4
                ? 'far fa-dot-circle text-xl absolute left-[3.4rem] text-[#044D73]'
                : 'fas fa-circle text-[0.5rem] absolute left-[3.78rem] text-gray-400',
            ]"
          ></i>
          <h1
            class=""
            :class="[
              year4 ? 'text-6xl' : 'text-4xl',
              'text-[#044D73]  font-bold font-serif ',
            ]"
          >
            1820
          </h1>
          <div class="w-[12rem]">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              :class="[year4 ? 'hidden' : '', 'h-12 w-[5rem] text-[#044D73]']"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 8l4 4m0 0l-4 4m4-4H3"
              />
            </svg>
          </div>
        </div>
        <p :class="[year4 ? '' : 'hidden', 'font-semibold']">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse sapiente
          reiciendis consequatur, magni error velit assumenda tempora quam?
          Corporis aliquam similique officiis doloremque molestias nesciunt,
          totam maiores quod minus consectetur non ipsa necessitatibus
          cupiditate aliquid tempore dolor, ullam possimus quia.
        </p>
      </div>
      <div class="border-l-2 pl-5 pb-3">
        <div
          class="flex items-center pb-6 cursor-pointer"
          v-on:click="toggle('year5')"
        >
          <i
            class=""
            :class="[
              year5
                ? 'far fa-dot-circle text-xl absolute left-[3.4rem] text-[#044D73]'
                : 'fas fa-circle text-[0.5rem] absolute left-[3.78rem] text-gray-400',
            ]"
          ></i>
          <h1
            class=""
            :class="[
              year5 ? 'text-6xl' : 'text-4xl',
              'text-[#044D73]  font-bold font-serif ',
            ]"
          >
            1830
          </h1>
          <div class="w-[12rem]">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              :class="[year5 ? 'hidden' : '', 'h-12 w-[5rem] text-[#044D73]']"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 8l4 4m0 0l-4 4m4-4H3"
              />
            </svg>
          </div>
        </div>
        <p :class="[year5 ? '' : 'hidden', 'font-semibold']">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni,
          veniam! Quas ipsam corrupti id inventore dolorum eum nemo minima
          placeat facere dolore quia delectus ullam excepturi molestiae unde,
          minus ad, ex consequuntur accusamus.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionTwo',
  data() {
    return {
      year1: false,
      year2: false,
      year3: false,
      year4: false,
      year5: false,
    };
  },
  methods: {
    toggle(year) {
      if (year == 'year1') {
        this.year1 = !this.year1;
        return;
      }
      if (year == 'year2') {
        this.year2 = !this.year2;
        return;
      }
      if (year == 'year3') {
        this.year3 = !this.year3;
        return;
      }
      if (year == 'year4') {
        this.year4 = !this.year4;
        return;
      }
      if (year == 'year5') {
        this.year5 = !this.year5;
        return;
      }
    },
  },
};
</script>

<style></style>
