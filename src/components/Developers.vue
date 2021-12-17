<template>
  <div class="relative bg-gray-200">
    <div class="custom-shape-divider-top-1637347312">
      <svg
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
      >
        <path
          d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
          class="shape-fill"
        />
      </svg>
    </div>
    <div class="container mx-auto">
      <div class="flex flex-row h-auto py-40 align-items-center flex-wrap">
        <div class="w-1/3 w-sm-full flex flex-col justify-center text-center">
          <div class="dev-photo mx-auto shadow-md rounded-md overflow-hidden">
            <img
              class
              src="https://images.pexels.com/photos/1024311/pexels-photo-1024311.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
              alt="dev-1"
            />
          </div>
          <h2
            class="text-black text-center pt-4 font-light text-3x1 sm:text-4xl md:text-3xl font-bold"
          >Angely T.</h2>
          <span
            class="text-indigo-600 text-center font-light text-base sm:text-3xl md:text-base font-bold"
          >Back-end Developer</span>
        </div>
        <div class="w-1/3 w-sm-ful flex flex-col justify-center text-center">
          <div class="dev-photo mx-auto shadow-md rounded-md overflow-hidden">
            <img
              class
              src="https://images.pexels.com/photos/871495/pexels-photo-871495.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
              alt="dev-1"
            />
          </div>
          <h2
            class="text-black text-center pt-4 font-light text-3x1 sm:text-4xl md:text-3xl font-bold"
          >Carla Q.</h2>
          <span
            class="text-indigo-600 text-center font-light text-base sm:text-3xl md:text-base font-bold"
          >Community Manager</span>
        </div>
        <div class="w-1/3 flex flex-col justify-center text-center">
          <router-link to="/developer" class="mx-auto shadow-md rounded-md overflow-hidden">
            <div class="dev-photo">
              <img
                class
                src="https://images.pexels.com/photos/2379004/pexels-photo-2379004.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
                alt="dev-1"
              />
            </div>
          </router-link>
          <h2
            class="text-black text-center pt-4 font-light text-3x1 sm:text-4xl md:text-3xl font-bold"
          >Edgardo G.</h2>
          <span
            class="text-indigo-600 text-center font-light text-base sm:text-3xl md:text-base font-bold"
          >UX/UI Expert</span>
        </div>

        <!-- Second Row -->
        <div class="w-1/3 mt-8 w-sm-ful flex flex-col justify-center text-center">
          <div class="dev-photo mx-auto shadow-md rounded-md overflow-hidden">
            <img
              class
              src="https://images.pexels.com/photos/3290236/pexels-photo-3290236.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
              alt="dev-1"
            />
          </div>
          <h2
            class="text-black text-center pt-4 font-light text-3x1 sm:text-4xl md:text-3xl font-bold"
          >Veronica S.</h2>
          <span
            class="text-indigo-600 text-center font-light text-base sm:text-3xl md:text-base font-bold"
          >Front-end Developer</span>
        </div>
        <div class="w-1/3 mt-8 w-sm-ful flex flex-col justify-center text-center">
          <div class="dev-photo mx-auto shadow-md rounded-md overflow-hidden">
            <img
              class
              src="https://images.pexels.com/photos/773371/pexels-photo-773371.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
              alt="dev-1"
            />
          </div>
          <h2
            class="text-black text-center pt-4 font-light text-3x1 sm:text-4xl md:text-3xl font-bold"
          >Alicia G.</h2>
          <span
            class="text-indigo-600 text-center font-light text-base sm:text-3xl md:text-base font-bold"
          >Project Manager</span>
        </div>
        <div class="w-1/3 mt-8 w-sm-ful flex flex-col justify-center text-center">
          <div class="dev-photo mx-auto shadow-md rounded-md overflow-hidden">
            <img
              class
              src="https://images.pexels.com/photos/1222271/pexels-photo-1222271.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
              alt="dev-1"
            />
          </div>
          <h2
            class="text-black text-center pt-4 font-light text-3x1 sm:text-4xl md:text-3xl font-bold"
          >Jesús P.</h2>
          <span
            class="text-indigo-600 text-center font-light text-base sm:text-3xl md:text-base font-bold"
          >Front-end Developer</span>
        </div>
      </div>
    </div>
    <div class="custom-shape-divider-bottom-1637347624">
      <svg
        fill="currentColor"
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
      >
        <path
          d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
          class="shape-fill"
        />
      </svg>
    </div>
  </div>
</template>

<script lang="ts">
export default {
}
</script>

<style>
.dev-photo img {
  object-fit: cover;
  width: 260px;
  height: 260px;
}

.custom-shape-divider-top-1637347312 {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  line-height: 0;
}

.custom-shape-divider-top-1637347312 svg,
.custom-shape-divider-bottom-1637347624 svg {
  position: relative;
  display: block;
  width: calc(100% + 1.3px);
  height: 150px;
}

.custom-shape-divider-top-1637347312 .shape-fill,
.custom-shape-divider-bottom-1637347624 .shape-fill {
  fill: #ffffff;
}

.custom-shape-divider-bottom-1637347624 {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  overflow: hidden;
  line-height: 0;
  transform: rotate(180deg);
}
</style>