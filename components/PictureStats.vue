<template>
  <div class="relative bg-gray-900">
    <div class="absolute bottom-0 h-80 w-full xl:inset-0 xl:h-full">
      <div class="h-full w-full xl:grid xl:grid-cols-2">
        <div class="h-full xl:relative xl:col-start-2">
          <img
            class="h-full w-full object-cover opacity-25 xl:absolute xl:inset-0"
            src="https://images.unsplash.com/photo-1626775238053-4315516eedc9?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2830&q=80&sat=-100"
            alt="People working on laptops"
          >
          <div
            aria-hidden="true"
            class="absolute inset-x-0 top-0 h-32 bg-gradient-to-b from-gray-900 xl:inset-y-0 xl:left-0 xl:h-full xl:w-32 xl:bg-gradient-to-r"
          />
        </div>
      </div>
    </div>
    <div
      class="mx-auto max-w-4xl px-4 sm:px-6 lg:max-w-7xl lg:px-8 xl:grid xl:grid-flow-col-dense xl:grid-cols-2 xl:gap-x-8"
    >
      <div class="relative pt-12 pb-64 sm:pt-24 sm:pb-64 xl:col-start-1 xl:pb-24">
        <h2 class="text-base font-semibold text-orange-300">
          No experience needed
        </h2>
        <p class="mt-3 text-3xl font-bold tracking-tight text-white">
          Learn to deal the most popular card games, taught by industry experts.
        </p>
        <p class="mt-5 text-lg text-gray-300">
          We have hand picked instructors with over
          two decades in the industry, who know the dealing world inside & out. Jump start your new career in less than 3 months - and learn how to deal from the best.
        </p>
        <div class="mt-12 grid grid-cols-1 gap-y-12 gap-x-6 sm:grid-cols-2">
          <p>
            <span class="block text-2xl font-bold text-white">2.6K+</span>
            <span class="mt-1 block text-base text-gray-300"><span class="font-medium text-white">Successful students</span> have used
              our course(s) to advance their career.</span>
          </p>

          <p>
            <span class="block text-2xl font-bold text-white">500+</span>
            <span class="mt-1 block text-base text-gray-300"><span class="font-medium text-white">Five-star reviews</span> from Coast Dealing Academy's alumni.</span>
          </p>

          <p>
            <span class="block text-2xl font-bold text-white">12+</span>
            <span class="mt-1 block text-base text-gray-300"><span class="font-medium text-white">Course paths</span>
              to fit your schedule and budget. Learn at your own pace!</span>
          </p>
          <p>
            <span class="block text-2xl font-bold text-white">99.5%</span>
            <span class="mt-1 block text-base text-gray-300"><span class="font-medium text-white">Job
              placement</span> at Mississippi's largest & highest-paying casinos.</span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PictureStats'
}
</script>
