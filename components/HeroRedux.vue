<template>
  <div class="bg-white">
    <!-- olD HEADER -->
    <div class="relative bg-white mb-12">
      <div class="mx-auto max-w-7xl px-4 sm:px-6">
        <div class="flex items-center justify-between py-6 md:justify-start md:space-x-10">
          <div class="flex justify-start lg:w-0 lg:flex-1">
            <a href="#">
              <span class="sr-only">Your Company</span>
              <img class="h-8 w-auto sm:h-20 sm:absolute top-2" src="~/static/cda-logo.png" alt="Coast Dealing Academy Logo">
            </a>
          </div>
          <div class="-my-2 -mr-2 md:hidden">
            <button
              type="button"
              class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-rose-500"
              aria-expanded="false"
            >
              <span class="sr-only">Open menu</span>
              <!-- Heroicon name: outline/bars-3 -->
              <svg
                class="h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
              </svg>
            </button>
          </div>
          <nav class="hidden space-x-10 md:flex">
            <div class="relative">
              <!-- Item active: "text-gray-900", Item inactive: "text-gray-500" -->
              <button
                type="button"
                class="text-gray-500 group inline-flex items-center rounded-md bg-white text-base font-medium hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-rose-500 focus:ring-offset-2"
                :aria-expanded="solutionsOpen"
                @click.prevent="solutionsOpen = true"
              >
                <span>Courses</span>
                <!--
                    Heroicon name: mini/chevron-down

                    Item active: "text-gray-600", Item inactive: "text-gray-400"
                  -->
                <svg
                  class="text-gray-400 ml-2 h-5 w-5 group-hover:text-gray-500"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>

              <!--
                  'Solutions' flyout menu, show/hide based on flyout menu state.

                  Entering: "transition ease-out duration-200"
                    From: "opacity-0 translate-y-1"
                    To: "opacity-100 translate-y-0"
                  Leaving: "transition ease-in duration-150"
                    From: "opacity-100 translate-y-0"
                    To: "opacity-0 translate-y-1"
                -->
              <solutions-open :open="solutionsOpen" @close="solutionsOpen = false" />
            </div>

            <a href="#" class="text-base font-medium text-gray-500 hover:text-gray-900">Pricing</a>
            <a href="#" class="text-base font-medium text-gray-500 hover:text-gray-900">Reviews</a>
            <a href="#" class="text-base font-medium text-gray-500 hover:text-gray-900">Contact</a>
            <div class="relative">
              <!-- Item active: "text-gray-900", Item inactive: "text-gray-500" -->
              <button
                type="button"
                class="text-gray-500 group inline-flex items-center rounded-md bg-white text-base font-medium hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-rose-500 focus:ring-offset-2"
                :aria-expanded="moreOpen"
                @click.prevent="moreOpen = true"
              >
                <span>More</span>
                <!--
                    Heroicon name: mini/chevron-down

                    Item active: "text-gray-600", Item inactive: "text-gray-400"
                  -->
                <svg
                  class="text-gray-400 ml-2 h-5 w-5 group-hover:text-gray-500"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>

              <!--
                  'More' flyout menu, show/hide based on flyout menu state.

                  Entering: "transition ease-out duration-200"
                    From: "opacity-0 translate-y-1"
                    To: "opacity-100 translate-y-0"
                  Leaving: "transition ease-in duration-150"
                    From: "opacity-100 translate-y-0"
                    To: "opacity-0 translate-y-1"
                -->
              <MoreOpen :open="moreOpen" @close="moreOpen = false" />
            </div>
          </nav>
          <div class="hidden items-center justify-end md:flex md:flex-1 lg:w-0">
            <a href="#" class="whitespace-nowrap text-base font-medium text-gray-500 hover:text-gray-900">Sign in</a>
            <a
              href="#"
              class="ml-8 inline-flex items-center justify-center whitespace-nowrap rounded-md border border-transparent bg-rose-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-rose-700"
            >Sign
              up</a>
          </div>
        </div>
      </div>

      <!--
          Mobile menu, show/hide based on mobile menu state.

          Entering: "duration-200 ease-out"
            From: "opacity-0 scale-95"
            To: "opacity-100 scale-100"
          Leaving: "duration-100 ease-in"
            From: "opacity-100 scale-100"
            To: "opacity-0 scale-95"
        -->
      <div class="absolute inset-x-0 top-0 z-10 origin-top-right transform p-2 transition md:hidden">
        <div class="divide-y-2 divide-gray-50 rounded-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5">
          <div class="px-5 pt-5 pb-6">
            <div class="flex items-center justify-between">
              <div>
                <img
                  class="h-8 w-auto"
                  src="https://tailwindui.com/img/logos/mark.svg?color=rose&shade=600"
                  alt="Your Company"
                >
              </div>
              <div class="-mr-2">
                <button
                  type="button"
                  class="inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-rose-500"
                >
                  <span class="sr-only">Close menu</span>
                  <!-- Heroicon name: outline/x-mark -->
                  <svg
                    class="h-6 w-6"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                </button>
              </div>
            </div>
            <div class="mt-6">
              <nav class="grid gap-y-8">
                <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
                  <!-- Heroicon name: outline/chart-bar -->
                  <svg
                    class="h-6 w-6 flex-shrink-0 text-rose-600"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M3 13.125C3 12.504 3.504 12 4.125 12h2.25c.621 0 1.125.504 1.125 1.125v6.75C7.5 20.496 6.996 21 6.375 21h-2.25A1.125 1.125 0 013 19.875v-6.75zM9.75 8.625c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125v11.25c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V8.625zM16.5 4.125c0-.621.504-1.125 1.125-1.125h2.25C20.496 3 21 3.504 21 4.125v15.75c0 .621-.504 1.125-1.125 1.125h-2.25a1.125 1.125 0 01-1.125-1.125V4.125z"
                    />
                  </svg>
                  <span class="ml-3 text-base font-medium text-gray-900">Analytics</span>
                </a>

                <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
                  <!-- Heroicon name: outline/cursor-arrow-rays -->
                  <svg
                    class="h-6 w-6 flex-shrink-0 text-rose-600"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M15.042 21.672L13.684 16.6m0 0l-2.51 2.225.569-9.47 5.227 7.917-3.286-.672zM12 2.25V4.5m5.834.166l-1.591 1.591M20.25 10.5H18M7.757 14.743l-1.59 1.59M6 10.5H3.75m4.007-4.243l-1.59-1.59"
                    />
                  </svg>
                  <span class="ml-3 text-base font-medium text-gray-900">Engagement</span>
                </a>

                <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
                  <!-- Heroicon name: outline/shield-check -->
                  <svg
                    class="h-6 w-6 flex-shrink-0 text-rose-600"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M9 12.75L11.25 15 15 9.75m-3-7.036A11.959 11.959 0 013.598 6 11.99 11.99 0 003 9.749c0 5.592 3.824 10.29 9 11.623 5.176-1.332 9-6.03 9-11.622 0-1.31-.21-2.571-.598-3.751h-.152c-3.196 0-6.1-1.248-8.25-3.285z"
                    />
                  </svg>
                  <span class="ml-3 text-base font-medium text-gray-900">Security</span>
                </a>

                <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
                  <!-- Heroicon name: outline/squares-2x2 -->
                  <svg
                    class="h-6 w-6 flex-shrink-0 text-rose-600"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M3.75 6A2.25 2.25 0 016 3.75h2.25A2.25 2.25 0 0110.5 6v2.25a2.25 2.25 0 01-2.25 2.25H6a2.25 2.25 0 01-2.25-2.25V6zM3.75 15.75A2.25 2.25 0 016 13.5h2.25a2.25 2.25 0 012.25 2.25V18a2.25 2.25 0 01-2.25 2.25H6A2.25 2.25 0 013.75 18v-2.25zM13.5 6a2.25 2.25 0 012.25-2.25H18A2.25 2.25 0 0120.25 6v2.25A2.25 2.25 0 0118 10.5h-2.25a2.25 2.25 0 01-2.25-2.25V6zM13.5 15.75a2.25 2.25 0 012.25-2.25H18a2.25 2.25 0 012.25 2.25V18A2.25 2.25 0 0118 20.25h-2.25A2.25 2.25 0 0113.5 18v-2.25z"
                    />
                  </svg>
                  <span class="ml-3 text-base font-medium text-gray-900">Integrations</span>
                </a>

                <a href="#" class="-m-3 flex items-center rounded-md p-3 hover:bg-gray-50">
                  <!-- Heroicon name: outline/arrow-path -->
                  <svg
                    class="h-6 w-6 flex-shrink-0 text-rose-600"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M4.5 12c0-1.232.046-2.453.138-3.662a4.006 4.006 0 013.7-3.7 48.678 48.678 0 017.324 0 4.006 4.006 0 013.7 3.7c.017.22.032.441.046.662M4.5 12l-3-3m3 3l3-3m12 3c0 1.232-.046 2.453-.138 3.662a4.006 4.006 0 01-3.7 3.7 48.657 48.657 0 01-7.324 0 4.006 4.006 0 01-3.7-3.7c-.017-.22-.032-.441-.046-.662M19.5 12l-3 3m3-3l3 3"
                    />
                  </svg>
                  <span class="ml-3 text-base font-medium text-gray-900">Automations</span>
                </a>
              </nav>
            </div>
          </div>
          <div class="space-y-6 py-6 px-5">
            <div class="grid grid-cols-2 gap-y-4 gap-x-8">
              <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700">Pricing</a>

              <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700">Docs</a>

              <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700">Help Center</a>

              <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700">Guides</a>

              <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700">Events</a>

              <a href="#" class="text-base font-medium text-gray-900 hover:text-gray-700">Security</a>
            </div>
            <div>
              <a
                href="#"
                class="flex w-full items-center justify-center rounded-md border border-transparent bg-rose-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-rose-700"
              >Sign
                up</a>
              <p class="mt-6 text-center text-base font-medium text-gray-500">
                Existing customer?
                <a href="#" class="text-rose-600 hover:text-rose-500">Sign in</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <main>
      <div>
        <!-- Hero card -->
        <div class="relative">
          <div class="absolute inset-x-0 bottom-0 h-1/2 bg-gray-100" />
          <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
            <div class="relative shadow-xl sm:overflow-hidden sm:rounded-2xl">
              <div class="absolute inset-0">
                <img
                  class="h-full w-full object-cover"
                  src="https://images.unsplash.com/photo-1446669052213-5dcff53f1f3f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2830&q=80&sat=-100"
                  alt="People working on laptops"
                >
                <div class="absolute inset-0 bg-rose-700 mix-blend-multiply" />
              </div>
              <div class="relative px-4 py-16 sm:px-6 sm:py-24 lg:py-32 lg:px-8">
                <h1 class="text-center text-4xl font-bold tracking-tight sm:text-5xl lg:text-6xl">
                  <span class="block text-white">The only casino school</span>
                  <span class="block text-rose-200">with guaranteed results.</span>
                </h1>
                <p class="mx-auto mt-6 max-w-lg text-center text-xl text-rose-200 sm:max-w-3xl">
                  Our instructors have trained casino staff for over two decades. Explore our various payment options or contact us to jump start your
                  career today.
                </p>
                <div class="mx-auto mt-10 max-w-sm sm:flex sm:max-w-none sm:justify-center">
                  <div class="space-y-4 sm:mx-auto sm:inline-grid sm:grid-cols-2 sm:gap-5 sm:space-y-0">
                    <a
                      href="#"
                      class="flex items-center justify-center rounded-md border border-transparent bg-white px-4 py-3 text-base font-medium text-rose-700 shadow-sm hover:bg-rose-50 sm:px-8"
                    >Get
                      started</a>
                    <a
                      href="#"
                      title="Show demo video"
                      class="flex items-center justify-center px-4 py-3 text-base font-medium text-white border border-transparent rounded-md shadow-sm bg-rose-500 bg-opacity-60 hover:bg-opacity-70 sm:px-8"
                    >
                      Watch video
                      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-5 h-5 ml-3 -mr-1">
                        <path
                          fill-rule="evenodd"
                          d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z"
                          clip-rule="evenodd"
                        />
                      </svg></a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Logo cloud -->
        <Features />
      </div>

      <!-- More main page content here... -->
    </main>
  </div>
</template>

<script>
export default {
  name: 'HeroRedux',
  data () {
    return {
      moreOpen: false,
      solutionsOpen: false
    }
  }
}
</script>
