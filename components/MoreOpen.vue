<template>
  <transition
    enter-active-class="transition duration-200 ease-out"
    enter-class="translate-y-1 opacity-0"
    enter-to-class="translate-y-0 opacity-100"
    leave-active-class="transition duration-150 ease-in"
    leave-class="translate-y-0 opacity-100"
    leave-to-class="translate-y-1 opacity-0"
  >
    <!--
    Flyout menu, show/hide based on flyout menu state.
  -->
    <div
      v-if="isOpen"
      v-click-outside="vcoConfig"
      class="absolute z-50 w-screen max-w-md px-2 mt-3 transform -translate-x-1/2 left-1/2 sm:px-0"
    >
      <div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5">
        <div class="relative grid gap-6 px-5 py-6 bg-white sm:gap-8 sm:p-8">
          <a href="#" class="flex items-start p-3 -m-3 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <!-- Heroicon name: outline/support -->
            <svg
              class="flex-shrink-0 w-6 h-6 text-rose-600"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"
              />
            </svg>
            <div class="ml-4">
              <p class="text-base font-medium text-gray-900">Help Center</p>
              <p class="mt-1 text-sm text-gray-500">Get all of your questions answered in our forums or contact support.
              </p>
            </div>
          </a>

          <a href="#" class="flex items-start p-3 -m-3 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <!-- Heroicon name: outline/bookmark-alt -->
            <svg
              class="flex-shrink-0 w-6 h-6 text-rose-600"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M16 4v12l-4-2-4 2V4M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"
              />
            </svg>
            <div class="ml-4">
              <p class="text-base font-medium text-gray-900">Guides</p>
              <p class="mt-1 text-sm text-gray-500">Learn how to maximize our platform to get the most out of it.</p>
            </div>
          </a>

          <a href="#" class="flex items-start p-3 -m-3 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <!-- Heroicon name: outline/calendar -->
            <svg
              class="flex-shrink-0 w-6 h-6 text-rose-600"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
              />
            </svg>
            <div class="ml-4">
              <p class="text-base font-medium text-gray-900">Events</p>
              <p class="mt-1 text-sm text-gray-500">See what meet-ups and other events we might be planning near you.
              </p>
            </div>
          </a>

          <a href="#" class="flex items-start p-3 -m-3 transition duration-150 ease-in-out rounded-lg hover:bg-gray-50">
            <!-- Heroicon name: outline/shield-check -->
            <svg
              class="flex-shrink-0 w-6 h-6 text-rose-600"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
              />
            </svg>
            <div class="ml-4">
              <p class="text-base font-medium text-gray-900">Security</p>
              <p class="mt-1 text-sm text-gray-500">Understand how we take your privacy seriously.</p>
            </div>
          </a>
        </div>
        <div class="px-5 py-5 bg-gray-50 sm:px-8 sm:py-8">
          <div>
            <h3 class="text-sm font-medium tracking-wide text-gray-500 uppercase">
              Recent Posts
            </h3>
            <ul role="list" class="mt-4 space-y-4">
              <li class="text-base truncate">
                <a href="#" class="font-medium text-gray-900 transition duration-150 ease-in-out hover:text-gray-700">
                  Boost your conversion rate </a>
              </li>

              <li class="text-base truncate">
                <a href="#" class="font-medium text-gray-900 transition duration-150 ease-in-out hover:text-gray-700">
                  How to use search engine optimization to drive traffic to your site </a>
              </li>

              <li class="text-base truncate">
                <a href="#" class="font-medium text-gray-900 transition duration-150 ease-in-out hover:text-gray-700">
                  Improve your customer experience </a>
              </li>
            </ul>
          </div>
          <div class="mt-5 text-sm">
            <a href="#" class="font-medium text-rose-600 transition duration-150 ease-in-out hover:text-rose-500"> View
              all posts <span aria-hidden="true">&rarr;</span></a>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
import vClickOutside from 'v-click-outside'
export default {
  directives: {
    clickOutside: vClickOutside.directive
  },
  props: {
    open: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return {
      isOpen: false
    }
  },
  computed: {
    vcoConfig () {
      return {
        handler: this.moreOpenMethod,
        events: ['click'],
        // activate / deactivate click-outside directive dynamically
        isActive: this.isOpen
      }
    }
  },
  watch: {
    open (newVal) {
      this.isOpen = newVal
    }
  },
  methods: {
    moreOpenMethod () {
      console.log('Working...')
      this.isOpen = false
      this.$emit('close')
    }
  }
}
</script>
