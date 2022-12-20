<template>
  <div class="relative overflow-hidden bg-gray-50">
    <div class="mx-auto max-w-7xl">
      <div class="relative z-10 pb-8 bg-gray-50 sm:pb-16 md:pb-20 lg:w-full lg:max-w-2xl lg:pb-28 xl:pb-32">
        <svg
          class="absolute inset-y-0 right-0 hidden w-48 h-full transform translate-x-1/2 text-gray-50 lg:block"
          fill="currentColor"
          viewBox="0 0 100 100"
          preserveAspectRatio="none"
          aria-hidden="true"
        >
          <polygon points="50,0 100,0 50,100 0,100" />
        </svg>

        <!-- spacer div-->
        <div class="w-full h-4 lg:h-12 bg-gray-50" />

        <main class="px-4 mx-auto mt-10 max-w-7xl sm:mt-12 sm:px-6 md:mt-16 lg:mt-20 lg:px-8 xl:mt-28">
          <!-- what's new bar-->
          <div>
            <a href="#" class="inline-flex space-x-4">
              <span class="rounded bg-rose-50 px-2.5 py-1 text-sm font-semibold text-rose-500">What's new</span>
              <span class="inline-flex items-center space-x-1 text-sm font-medium text-rose-500">
                <span>New payment plans</span>
                <!-- Heroicon name: mini/chevron-right -->
                <svg
                  class="w-5 h-5"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M7.21 14.77a.75.75 0 01.02-1.06L11.168 10 7.23 6.29a.75.75 0 111.04-1.08l4.5 4.25a.75.75 0 010 1.08l-4.5 4.25a.75.75 0 01-1.06-.02z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
            </a>
          </div>
          <div class="mt-4 sm:text-center lg:text-left">
            <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl md:text-6xl">
              <span class="block xl:inline">The casino school</span>
              <span class="block text-orange-600 xl:inline">that works for you.</span>
            </h1>
            <p class="mt-3 text-base text-gray-500 sm:mx-auto sm:mt-5 sm:max-w-xl sm:text-lg md:mt-5 md:text-xl lg:mx-0">
              Our school offers comprehensive training programs to help you succeed in the exciting world of casino dealing.
            </p>
            <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
              <div class="rounded-md shadow">
                <a
                  href="#"
                  class="flex items-center justify-center w-full px-8 py-3 text-base font-medium text-white bg-orange-600 border border-transparent rounded-md hover:bg-orange-700 md:py-4 md:px-10 md:text-lg"
                >Get
                  started</a>
              </div>
              <div class="mt-3 sm:mt-0 sm:ml-3">
                <a
                  href="#"
                  class="flex items-center justify-center w-full px-8 py-3 text-base font-medium text-orange-700 bg-orange-100 border border-transparent rounded-md hover:bg-orange-200 md:py-4 md:px-10 md:text-lg"
                >Live
                  demo</a>
              </div>
            </div>
          </div>
        </main>
      </div>
    </div>
    <div class="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
      <img
        class="object-cover w-full h-56 sm:h-72 md:h-96 lg:h-full lg:w-full"
        src="https://images.unsplash.com/photo-1611104866937-e7e05b8571b7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2850&q=70"
        alt=""
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'AngledHero'
}
</script>
