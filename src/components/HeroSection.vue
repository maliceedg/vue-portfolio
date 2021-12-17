<template>
  <div class="mx-0 w-full h-full bg-light-600 overflow-hidden">
    <div class="h-150 hero-bg flex flex-row justify-between">
      <div class="overlay"></div>
      <div class="w-1/2 h-auto flex flex-col justify-center justify-items-center relative">
        <div class="container mx-auto pl-6 z-5">
          <h2
            class="z-10 self-start text-left text-3x1 sm:text-3xl md:text-6xl font-extrabold text-white"
          >
            Hello, and welcome
            <br />to WorkFlow
          </h2>
          <h2
            class="text-indigo-600 self-start text-left text-3x1 sm:text-3xl md:text-4xl font-extrabold"
          >Enrich yourself</h2>
        </div>
        <div class="w-150 flex justify-start pl-6 pt-10 z-5">
          <button
            type="button"
            class="group relative w-40 flex justify-center py-2 px-4 border border-transparent text-md font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            Join Today
            <span class="absolute right-0 inset-y-0 flex items-center pl-3 text-light-50">
              <!-- Heroicon name: solid/lock-closed -->
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="text-white mr-3"
                fill="currentColor"
                width="18"
                height="18"
                viewBox="0 0 24 24"
              >
                <path d="M6.028 0v6.425l5.549 5.575-5.549 5.575v6.425l11.944-12z" />
              </svg>
            </span>
          </button>

          <button
            type="button"
            class="group relative w-40 flex justify-center ml-4 py-2 px-4 border border-transparent text-md font-medium rounded-md text-white bg-indigo-400 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >Keep Looking</button>
        </div>
      </div>
      <div class="w-1/2">
        <!-- <img
          class="hero-image"
          src="https://images.pexels.com/photos/574071/pexels-photo-574071.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"
          alt="develop"
        />-->
        <svg
          class="z-5"
          xmlns="http://www.w3.org/2000/svg"
          version="1.1"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          xmlns:svgjs="http://svgjs.com/svgjs"
          width="1024"
          height="560"
          preserveAspectRatio="none"
          viewBox="0 0 1024 560"
        >
          <g mask="url(&quot;#SvgjsMask1009&quot;)" fill="none">
            <path
              d="M1285.705444455067 257.6481051768197L1191.105087842132 140.82639378830433 1168.8837330665517 352.2484617897548z"
              fill="rgba(79, 70, 229, 0.6)"
              class="triangle-float2"
            />
            <path
              d="M381.56,561.772C416.132,561.041,456.002,560.281,473.058,530.2C489.988,500.24,469.52,466.224,452.699,436.302C435.365,405.466,416.919,368.46,381.56,367.433C345.224,366.378,321.362,400.646,302.883,431.95C283.967,463.995,263.824,502.39,283.11,534.214C302.04,565.45,345.043,562.544,381.56,561.772"
              fill="rgba(79, 70, 229, 0.6)"
              class="triangle-float2"
            />
            <path
              d="M546.6551500636733 72.70305463136378L476.8664655032285 21.998607324649512 426.1620181965142 91.78729188509433 495.95070275695906 142.49173919180862z"
              fill="rgba(79, 70, 229, 0.6)"
              class="triangle-float3"
            />
            <path
              d="M140.89402355400424 91.75570089625879L97.62637575219034 48.48805309444491 54.358727950376476 135.0233486980727z"
              fill="rgba(79, 70, 229, 0.6)"
              class="triangle-float2"
            />
            <path
              d="M787.8189992510249 195.87860206238378L924.6916620591401 123.10211631068763 851.915176307444-13.770546497427574 715.0425134993288 59.00593925426858z"
              fill="rgba(79, 70, 229, 0.6)"
              class="triangle-float3"
            />
            <path
              d="M106.501,558.153C147.607,561.735,195.323,560.046,217.14,525.024C239.71,488.794,224.542,442.183,200.875,406.66C179.929,375.221,144.276,358.481,106.501,358.962C69.618,359.431,33.89,376.643,16.197,409.009C-0.878,440.244,6.441,477.82,24.879,508.271C42.58,537.505,72.455,555.186,106.501,558.153"
              fill="rgba(79, 70, 229, 0.6)"
              class="triangle-float1"
            />
          </g>
          <defs>
            <mask id="SvgjsMask1009">
              <rect width="680" height="560" fill="#ffffff" />
            </mask>
          </defs>
        </svg>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style>
.hero-bg {
  z-index: 5;
  background-size: cover;
  background-repeat: no-repeat;
  background-image: url("../../public/developer.jpeg");
}

.overlay {
  height: 80%;
  width: 100%;
  background: rgb(2, 0, 36);
  background: linear-gradient(
    270deg,
    rgba(2, 0, 36, 0.7) 0%,
    rgba(255, 255, 255, 0) 100%
  );
  position: absolute;
  z-index: 1;
}

.animated-bg {
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' version='1.1' xmlns:xlink='http://www.w3.org/1999/xlink' xmlns:svgjs='http://svgjs.com/svgjs' width='1440' height='560' preserveAspectRatio='none' viewBox='0 0 1440 560'%3e%3cg mask='url(%26quot%3b%23SvgjsMask1009%26quot%3b)' fill='none'%3e%3cpath d='M1285.705444455067 257.6481051768197L1191.105087842132 140.82639378830433 1168.8837330665517 352.2484617897548z' fill='rgba(0%2c 0%2c 13%2c 0.2)' class='triangle-float2'%3e%3c/path%3e%3cpath d='M381.56%2c561.772C416.132%2c561.041%2c456.002%2c560.281%2c473.058%2c530.2C489.988%2c500.24%2c469.52%2c466.224%2c452.699%2c436.302C435.365%2c405.466%2c416.919%2c368.46%2c381.56%2c367.433C345.224%2c366.378%2c321.362%2c400.646%2c302.883%2c431.95C283.967%2c463.995%2c263.824%2c502.39%2c283.11%2c534.214C302.04%2c565.45%2c345.043%2c562.544%2c381.56%2c561.772' fill='rgba(0%2c 0%2c 13%2c 0.2)' class='triangle-float2'%3e%3c/path%3e%3cpath d='M546.6551500636733 72.70305463136378L476.8664655032285 21.998607324649512 426.1620181965142 91.78729188509433 495.95070275695906 142.49173919180862z' fill='rgba(0%2c 0%2c 13%2c 0.2)' class='triangle-float3'%3e%3c/path%3e%3cpath d='M140.89402355400424 91.75570089625879L97.62637575219034 48.48805309444491 54.358727950376476 135.0233486980727z' fill='rgba(0%2c 0%2c 13%2c 0.2)' class='triangle-float2'%3e%3c/path%3e%3cpath d='M787.8189992510249 195.87860206238378L924.6916620591401 123.10211631068763 851.915176307444-13.770546497427574 715.0425134993288 59.00593925426858z' fill='rgba(0%2c 0%2c 13%2c 0.2)' class='triangle-float3'%3e%3c/path%3e%3cpath d='M106.501%2c558.153C147.607%2c561.735%2c195.323%2c560.046%2c217.14%2c525.024C239.71%2c488.794%2c224.542%2c442.183%2c200.875%2c406.66C179.929%2c375.221%2c144.276%2c358.481%2c106.501%2c358.962C69.618%2c359.431%2c33.89%2c376.643%2c16.197%2c409.009C-0.878%2c440.244%2c6.441%2c477.82%2c24.879%2c508.271C42.58%2c537.505%2c72.455%2c555.186%2c106.501%2c558.153' fill='rgba(0%2c 0%2c 13%2c 0.2)' class='triangle-float1'%3e%3c/path%3e%3c/g%3e%3cdefs%3e%3cmask id='SvgjsMask1009'%3e%3crect width='1440' height='560' fill='white'%3e%3c/rect%3e%3c/mask%3e%3cstyle%3e %40keyframes float1 %7b 0%25%7btransform: translate(0%2c 0)%7d 50%25%7btransform: translate(-10px%2c 0)%7d 100%25%7btransform: translate(0%2c 0)%7d %7d .triangle-float1 %7b animation: float1 5s infinite%3b %7d %40keyframes float2 %7b 0%25%7btransform: translate(0%2c 0)%7d 50%25%7btransform: translate(-5px%2c -5px)%7d 100%25%7btransform: translate(0%2c 0)%7d %7d .triangle-float2 %7b animation: float2 4s infinite%3b %7d %40keyframes float3 %7b 0%25%7btransform: translate(0%2c 0)%7d 50%25%7btransform: translate(0%2c -10px)%7d 100%25%7btransform: translate(0%2c 0)%7d %7d .triangle-float3 %7b animation: float3 6s infinite%3b %7d %3c/style%3e%3c/defs%3e%3c/svg%3e");
}

@keyframes float1 {
  0% {
    transform: translate(0, 0);
  }
  50% {
    transform: translate(-10px, 0);
  }
  100% {
    transform: translate(0, 0);
  }
}

.triangle-float1 {
  animation: float1 5s infinite;
}

@keyframes float2 {
  0% {
    transform: translate(0, 0);
  }
  50% {
    transform: translate(-5px, -5px);
  }
  100% {
    transform: translate(0, 0);
  }
}

.triangle-float2 {
  animation: float2 4s infinite;
}

@keyframes float3 {
  0% {
    transform: translate(0, 0);
  }
  50% {
    transform: translate(0, -10px);
  }
  100% {
    transform: translate(0, 0);
  }
}

.triangle-float3 {
  animation: float3 6s infinite;
}
</style>